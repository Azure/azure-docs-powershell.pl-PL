---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704771"
---
# <span data-ttu-id="69c9d-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="69c9d-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="69c9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="69c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="69c9d-103">Umożliwia zbieranie danych w celu usprawnienia środowiska użytkownika za pomocą poleceń cmdlet usługi AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="69c9d-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="69c9d-104">Wykonanie tego polecenia cmdlet umożliwia zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="69c9d-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="69c9d-105">Nie są zbierane żadne dane, o ile użytkownik wyraźnie nie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="69c9d-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="69c9d-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="69c9d-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69c9d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="69c9d-107">DESCRIPTION</span></span>
<span data-ttu-id="69c9d-108">Możesz ulepszyć środowisko korzystania z usługi Microsoft Cloud i Azure PowerShell, wybierając do kolekcji danych.</span><span class="sxs-lookup"><span data-stu-id="69c9d-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="69c9d-109">Program Azure PowerShell nie gromadzi danych bez zgody użytkownika — należy wyraźnie włączyć, wykonując polecenie Włącz-AzDataCollection lub odpowiedzi tak, gdy program Azure PowerShell wyświetli monit o zbieranie danych przy pierwszym uruchomieniu polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69c9d-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="69c9d-110">Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania w celu zidentyfikowania typowych problemów i usprawnienia korzystania z usługi Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="69c9d-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="69c9d-111">Program Microsoft Azure PowerShell nie gromadzi żadnych danych prywatnych ani żadnych informacji umożliwiających identyfikację użytkownika.</span><span class="sxs-lookup"><span data-stu-id="69c9d-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="69c9d-112">Uruchom polecenie cmdlet Enable-AzDataCollection, aby włączyć zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="69c9d-112">Run the Enable-AzDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="69c9d-113">Zapobiegnie to monitowaniu bieżącego użytkownika o zbieranie danych przy pierwszym uruchomieniu poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69c9d-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="69c9d-114">Aby wyłączyć zbieranie danych dla bieżącego użytkownika, uruchom polecenie cmdlet Disable-AzDataCollection.</span><span class="sxs-lookup"><span data-stu-id="69c9d-114">To disable data collection for the current user, run the Disable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="69c9d-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="69c9d-115">EXAMPLES</span></span>

### <span data-ttu-id="69c9d-116">Przykład 1: Włączanie zbierania danych dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="69c9d-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzDataCollection
```

<span data-ttu-id="69c9d-117">W tym przykładzie pokazano, jak włączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="69c9d-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="69c9d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="69c9d-118">PARAMETERS</span></span>

### <span data-ttu-id="69c9d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69c9d-119">-DefaultProfile</span></span>
<span data-ttu-id="69c9d-120">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="69c9d-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69c9d-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="69c9d-121">-Confirm</span></span>
<span data-ttu-id="69c9d-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69c9d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69c9d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69c9d-123">-WhatIf</span></span>
<span data-ttu-id="69c9d-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69c9d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69c9d-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="69c9d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69c9d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69c9d-126">CommonParameters</span></span>
<span data-ttu-id="69c9d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69c9d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69c9d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69c9d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69c9d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="69c9d-129">INPUTS</span></span>

### <span data-ttu-id="69c9d-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="69c9d-130">None</span></span>

## <span data-ttu-id="69c9d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="69c9d-131">OUTPUTS</span></span>

### <span data-ttu-id="69c9d-132">System. void</span><span class="sxs-lookup"><span data-stu-id="69c9d-132">System.Void</span></span>

## <span data-ttu-id="69c9d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="69c9d-133">NOTES</span></span>

## <span data-ttu-id="69c9d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="69c9d-134">RELATED LINKS</span></span>

[<span data-ttu-id="69c9d-135">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="69c9d-135">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)

