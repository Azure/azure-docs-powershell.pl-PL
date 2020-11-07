---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: e78a361bfb332bc2a8bcb226fae946a3abc0a05d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707237"
---
# <span data-ttu-id="ca538-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ca538-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="ca538-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca538-102">SYNOPSIS</span></span>
<span data-ttu-id="ca538-103">Nie możesz zbierać danych, aby ulepszyć polecenia cmdlet usługi AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca538-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="ca538-104">Dane nie są zbierane, jeśli użytkownik wyraźnie nie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="ca538-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="ca538-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca538-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca538-106">Opis</span><span class="sxs-lookup"><span data-stu-id="ca538-106">DESCRIPTION</span></span>
<span data-ttu-id="ca538-107">Możesz ulepszyć środowisko korzystania z usługi Microsoft Cloud i Azure PowerShell, wybierając do kolekcji danych.</span><span class="sxs-lookup"><span data-stu-id="ca538-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="ca538-108">Program Azure PowerShell nie gromadzi danych bez zgody użytkownika — należy wyraźnie włączyć, wykonując polecenie Włącz-AzDataCollection lub odpowiedzi tak, gdy program Azure PowerShell wyświetli monit o zbieranie danych przy pierwszym uruchomieniu polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca538-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="ca538-109">Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania w celu zidentyfikowania typowych problemów i usprawnienia korzystania z usługi Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="ca538-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="ca538-110">Program Microsoft Azure PowerShell nie gromadzi żadnych danych prywatnych ani żadnych informacji umożliwiających identyfikację użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ca538-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="ca538-111">Uruchom polecenie cmdlet Disable-AzDataCollection, aby wyłączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ca538-111">Run the Disable-AzDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="ca538-112">Zapobiegnie to monitowaniu bieżącego użytkownika o zbieranie danych przy pierwszym uruchomieniu poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca538-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="ca538-113">Aby włączyć zbieranie danych dla bieżącego użytkownika, uruchom polecenie cmdlet Enable-AzDataCollection.</span><span class="sxs-lookup"><span data-stu-id="ca538-113">To enable data collection for the current user, run the Enable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="ca538-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca538-114">EXAMPLES</span></span>

### <span data-ttu-id="ca538-115">Przykład 1: wyłączanie zbierania danych dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="ca538-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzDataCollection
```

<span data-ttu-id="ca538-116">W tym przykładzie pokazano, jak wyłączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ca538-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="ca538-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca538-117">PARAMETERS</span></span>

### <span data-ttu-id="ca538-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca538-118">-DefaultProfile</span></span>
<span data-ttu-id="ca538-119">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca538-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca538-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca538-120">-Confirm</span></span>
<span data-ttu-id="ca538-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca538-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca538-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca538-122">-WhatIf</span></span>
<span data-ttu-id="ca538-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca538-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca538-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ca538-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca538-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca538-125">CommonParameters</span></span>
<span data-ttu-id="ca538-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca538-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca538-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca538-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca538-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca538-128">INPUTS</span></span>

### <span data-ttu-id="ca538-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ca538-129">None</span></span>

## <span data-ttu-id="ca538-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca538-130">OUTPUTS</span></span>

### <span data-ttu-id="ca538-131">System. void</span><span class="sxs-lookup"><span data-stu-id="ca538-131">System.Void</span></span>

## <span data-ttu-id="ca538-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca538-132">NOTES</span></span>

## <span data-ttu-id="ca538-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca538-133">RELATED LINKS</span></span>

[<span data-ttu-id="ca538-134">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="ca538-134">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

