---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 2F3BDDFE-7585-4802-BFA5-D110F846A33E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/Remove-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 9ba839bbfc6740d9d62c9a036d233a8b5a1ce0e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552295"
---
# <span data-ttu-id="d34ef-101">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d34ef-101">Remove-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="d34ef-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d34ef-102">SYNOPSIS</span></span>
<span data-ttu-id="d34ef-103">Umożliwia usunięcie zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d34ef-103">Removes a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d34ef-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d34ef-104">SYNTAX</span></span>

```
Remove-AzureRmStreamAnalyticsJob [-Name] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d34ef-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d34ef-105">DESCRIPTION</span></span>
<span data-ttu-id="d34ef-106">Polecenie cmdlet **Remove-AzureRmStreamAnalyticsJob** asynchronicznie usuwa określone zadanie analizy strumienia na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d34ef-106">The **Remove-AzureRmStreamAnalyticsJob** cmdlet asynchronously deletes a specific Stream Analytics job in Azure.</span></span>

## <span data-ttu-id="d34ef-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d34ef-107">EXAMPLES</span></span>

### <span data-ttu-id="d34ef-108">PRZYKŁAD 1: usuwanie zadania</span><span class="sxs-lookup"><span data-stu-id="d34ef-108">EXAMPLE 1: Remove a job</span></span>
```
PS C:\>Remove-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -Name "StreamingJob"
```

<span data-ttu-id="d34ef-109">To polecenie usuwa zadanie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="d34ef-109">This command removes the job StreamingJob.</span></span>

## <span data-ttu-id="d34ef-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d34ef-110">PARAMETERS</span></span>

### <span data-ttu-id="d34ef-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d34ef-111">-Name</span></span>
<span data-ttu-id="d34ef-112">Określa nazwę zadania usługi Azure Stream Analytics, które należy usunąć.</span><span class="sxs-lookup"><span data-stu-id="d34ef-112">Specifies the name of the Azure Stream Analytics job to remove.</span></span>

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

### <span data-ttu-id="d34ef-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34ef-113">-ResourceGroupName</span></span>
<span data-ttu-id="d34ef-114">Określa nazwę grupy zasobów, do której należy zadanie usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d34ef-114">Specifies the name of the resource group to which the Azure Stream Analytics job belongs.</span></span>

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

### <span data-ttu-id="d34ef-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d34ef-115">-Confirm</span></span>
<span data-ttu-id="d34ef-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d34ef-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d34ef-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34ef-117">-WhatIf</span></span>
<span data-ttu-id="d34ef-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d34ef-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d34ef-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d34ef-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d34ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34ef-120">-DefaultProfile</span></span>
<span data-ttu-id="d34ef-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d34ef-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d34ef-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34ef-122">CommonParameters</span></span>
<span data-ttu-id="d34ef-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34ef-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34ef-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d34ef-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34ef-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d34ef-125">INPUTS</span></span>

## <span data-ttu-id="d34ef-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d34ef-126">OUTPUTS</span></span>

### <span data-ttu-id="d34ef-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="d34ef-127">System.Object</span></span>

## <span data-ttu-id="d34ef-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d34ef-128">NOTES</span></span>

## <span data-ttu-id="d34ef-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d34ef-129">RELATED LINKS</span></span>

[<span data-ttu-id="d34ef-130">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d34ef-130">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d34ef-131">Nowe — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d34ef-131">New-AzureRmStreamAnalyticsJob</span></span>](./New-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d34ef-132">Start — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d34ef-132">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d34ef-133">Zatrzymaj — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d34ef-133">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


