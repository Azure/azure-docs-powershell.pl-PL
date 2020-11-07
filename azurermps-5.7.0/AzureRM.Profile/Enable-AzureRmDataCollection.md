---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 9a6e87fb28fde1af024460a0b09d0339222d1ee8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717723"
---
# <span data-ttu-id="3dabd-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="3dabd-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="3dabd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3dabd-102">SYNOPSIS</span></span>
<span data-ttu-id="3dabd-103">Umożliwia zbieranie danych w celu usprawnienia środowiska użytkownika za pomocą poleceń cmdlet usługi AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="3dabd-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="3dabd-104">Wykonanie tego polecenia cmdlet umożliwia zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="3dabd-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="3dabd-105">Nie są zbierane żadne dane, o ile użytkownik wyraźnie nie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="3dabd-105">No data is collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3dabd-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3dabd-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3dabd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3dabd-107">DESCRIPTION</span></span>
<span data-ttu-id="3dabd-108">Możesz ulepszyć środowisko korzystania z usługi Microsoft Cloud i Azure PowerShell, wybierając do kolekcji danych.</span><span class="sxs-lookup"><span data-stu-id="3dabd-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="3dabd-109">Program Azure PowerShell nie gromadzi danych bez zgody użytkownika — należy wyraźnie włączyć, wykonując polecenie Włącz-AzureRmDataCollection lub odpowiedzi tak, gdy program Azure PowerShell wyświetli monit o zbieranie danych przy pierwszym uruchomieniu polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dabd-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="3dabd-110">Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania w celu zidentyfikowania typowych problemów i usprawnienia korzystania z usługi Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3dabd-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="3dabd-111">Program Microsoft Azure PowerShell nie gromadzi żadnych danych prywatnych ani żadnych informacji umożliwiających identyfikację użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3dabd-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="3dabd-112">Uruchom polecenie cmdlet Enable-AzureRMDataCollection, aby włączyć zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="3dabd-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="3dabd-113">Zapobiegnie to monitowaniu bieżącego użytkownika o zbieranie danych przy pierwszym uruchomieniu poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dabd-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="3dabd-114">Aby wyłączyć zbieranie danych dla bieżącego użytkownika, uruchom polecenie cmdlet Disable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="3dabd-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="3dabd-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3dabd-115">EXAMPLES</span></span>

### <span data-ttu-id="3dabd-116">Przykład 1: Włączanie zbierania danych dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="3dabd-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="3dabd-117">W tym przykładzie pokazano, jak włączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3dabd-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="3dabd-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3dabd-118">PARAMETERS</span></span>

### <span data-ttu-id="3dabd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dabd-119">-DefaultProfile</span></span>
<span data-ttu-id="3dabd-120">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3dabd-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dabd-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3dabd-121">-Confirm</span></span>
<span data-ttu-id="3dabd-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dabd-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dabd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dabd-123">-WhatIf</span></span>
<span data-ttu-id="3dabd-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3dabd-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3dabd-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3dabd-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dabd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dabd-126">CommonParameters</span></span>
<span data-ttu-id="3dabd-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dabd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dabd-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3dabd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dabd-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3dabd-129">INPUTS</span></span>

### <span data-ttu-id="3dabd-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3dabd-130">None</span></span>
<span data-ttu-id="3dabd-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3dabd-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3dabd-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3dabd-132">OUTPUTS</span></span>

### <span data-ttu-id="3dabd-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3dabd-133">None</span></span>

## <span data-ttu-id="3dabd-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3dabd-134">NOTES</span></span>

## <span data-ttu-id="3dabd-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3dabd-135">RELATED LINKS</span></span>

[<span data-ttu-id="3dabd-136">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="3dabd-136">Disable-AzureRmDataCollection</span></span>](./Disable-AzureRmDataCollection.md)

