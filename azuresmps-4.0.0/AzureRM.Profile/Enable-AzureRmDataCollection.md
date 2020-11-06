---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523409"
---
# <span data-ttu-id="fe3f6-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="fe3f6-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="fe3f6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe3f6-103">Umożliwia zbieranie danych w celu usprawnienia środowiska użytkownika za pomocą poleceń cmdlet usługi AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="fe3f6-104">Wykonanie tego polecenia cmdlet umożliwia zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="fe3f6-105">Nie są zbierane żadne dane, o ile użytkownik wyraźnie nie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="fe3f6-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe3f6-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe3f6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe3f6-107">DESCRIPTION</span></span>
<span data-ttu-id="fe3f6-108">Możesz ulepszyć środowisko korzystania z usługi Microsoft Cloud i Azure PowerShell, wybierając do kolekcji danych.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="fe3f6-109">Program Azure PowerShell nie gromadzi danych bez zgody użytkownika — należy wyraźnie włączyć, wykonując polecenie Włącz-AzureRmDataCollection lub odpowiedzi tak, gdy program Azure PowerShell wyświetli monit o zbieranie danych przy pierwszym uruchomieniu polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="fe3f6-110">Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania w celu zidentyfikowania typowych problemów i usprawnienia korzystania z usługi Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="fe3f6-111">Program Microsoft Azure PowerShell nie gromadzi żadnych danych prywatnych ani żadnych informacji umożliwiających identyfikację użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="fe3f6-112">Uruchom polecenie cmdlet Enable-AzureRMDataCollection, aby włączyć zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="fe3f6-113">Zapobiegnie to monitowaniu bieżącego użytkownika o zbieranie danych przy pierwszym uruchomieniu poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="fe3f6-114">Aby wyłączyć zbieranie danych dla bieżącego użytkownika, uruchom polecenie cmdlet Disable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="fe3f6-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe3f6-115">EXAMPLES</span></span>

### <span data-ttu-id="fe3f6-116">Przykład 1: Włączanie zbierania danych dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="fe3f6-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="fe3f6-117">W tym przykładzie pokazano, jak włączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="fe3f6-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe3f6-118">PARAMETERS</span></span>

### <span data-ttu-id="fe3f6-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe3f6-119">-Confirm</span></span>
<span data-ttu-id="fe3f6-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe3f6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe3f6-121">-WhatIf</span></span>
<span data-ttu-id="fe3f6-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe3f6-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe3f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe3f6-124">CommonParameters</span></span>
<span data-ttu-id="fe3f6-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe3f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe3f6-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe3f6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe3f6-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe3f6-127">INPUTS</span></span>

## <span data-ttu-id="fe3f6-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe3f6-128">OUTPUTS</span></span>

### <span data-ttu-id="fe3f6-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fe3f6-129">None</span></span>

## <span data-ttu-id="fe3f6-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe3f6-130">NOTES</span></span>

## <span data-ttu-id="fe3f6-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe3f6-131">RELATED LINKS</span></span>

[<span data-ttu-id="fe3f6-132">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="fe3f6-132">Disable-AzureRmDataCollection</span></span>]()

