---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleSchedule.md
ms.openlocfilehash: 52f929cea9f2017ad6a2c2ea16475ec7d5d8a5a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063465"
---
# <span data-ttu-id="d757a-101">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d757a-101">New-AzScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d757a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d757a-102">SYNOPSIS</span></span>
<span data-ttu-id="d757a-103">Tworzy obiekt typu harmonogram</span><span class="sxs-lookup"><span data-stu-id="d757a-103">Creates an object of type Schedule</span></span>

## <span data-ttu-id="d757a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d757a-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleSchedule -FrequencyInMinutes <Int32> -TimeWindowInMinutes <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d757a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d757a-105">DESCRIPTION</span></span>
<span data-ttu-id="d757a-106">Tworzy obiekt typu harmonogram.</span><span class="sxs-lookup"><span data-stu-id="d757a-106">Creates an object of type Schedule.</span></span>
<span data-ttu-id="d757a-107">Ten obiekt ma zostać przekazany do polecenia, które umożliwia utworzenie reguły alertów dziennika.</span><span class="sxs-lookup"><span data-stu-id="d757a-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="d757a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d757a-108">EXAMPLES</span></span>

### <span data-ttu-id="d757a-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d757a-109">Example 1</span></span>
```powershell
PS C:\>  $schedule = New-AzScheduledQueryRuleSchedule -FrequencyInMinutes 15 -TimeWindowInMinutes 15
```

## <span data-ttu-id="d757a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d757a-110">PARAMETERS</span></span>

### <span data-ttu-id="d757a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d757a-111">-DefaultProfile</span></span>
<span data-ttu-id="d757a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d757a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d757a-113">-FrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="d757a-113">-FrequencyInMinutes</span></span>
<span data-ttu-id="d757a-114">Częstotliwość alertów</span><span class="sxs-lookup"><span data-stu-id="d757a-114">The alert frequency</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d757a-115">-TimeWindowInMinutes</span><span class="sxs-lookup"><span data-stu-id="d757a-115">-TimeWindowInMinutes</span></span>
<span data-ttu-id="d757a-116">Okno czas alertu</span><span class="sxs-lookup"><span data-stu-id="d757a-116">The alert time window</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d757a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d757a-117">CommonParameters</span></span>
<span data-ttu-id="d757a-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d757a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d757a-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d757a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d757a-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d757a-120">INPUTS</span></span>

### <span data-ttu-id="d757a-121">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d757a-121">None</span></span>

## <span data-ttu-id="d757a-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d757a-122">OUTPUTS</span></span>

### <span data-ttu-id="d757a-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="d757a-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleSchedule</span></span>

## <span data-ttu-id="d757a-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d757a-124">NOTES</span></span>

## <span data-ttu-id="d757a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d757a-125">RELATED LINKS</span></span>
