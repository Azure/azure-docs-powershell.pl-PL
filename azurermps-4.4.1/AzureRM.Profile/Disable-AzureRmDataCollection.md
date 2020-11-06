---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: ada6b5050a2a08af89720aa3afeaf1dcd876768a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546135"
---
# <span data-ttu-id="94f58-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="94f58-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="94f58-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="94f58-102">SYNOPSIS</span></span>
<span data-ttu-id="94f58-103">Nie możesz zbierać danych, aby ulepszyć polecenia cmdlet usługi AzurePowerShell.</span><span class="sxs-lookup"><span data-stu-id="94f58-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="94f58-104">Dane nie są zbierane, jeśli użytkownik wyraźnie nie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="94f58-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94f58-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="94f58-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94f58-106">Opis</span><span class="sxs-lookup"><span data-stu-id="94f58-106">DESCRIPTION</span></span>
<span data-ttu-id="94f58-107">Możesz ulepszyć środowisko korzystania z usługi Microsoft Cloud i Azure PowerShell, wybierając do kolekcji danych.</span><span class="sxs-lookup"><span data-stu-id="94f58-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="94f58-108">Program Azure PowerShell nie gromadzi danych bez zgody użytkownika — należy wyraźnie włączyć, wykonując polecenie Włącz-AzureRmDataCollection lub odpowiedzi tak, gdy program Azure PowerShell wyświetli monit o zbieranie danych przy pierwszym uruchomieniu polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f58-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="94f58-109">Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania w celu zidentyfikowania typowych problemów i usprawnienia korzystania z usługi Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="94f58-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="94f58-110">Program Microsoft Azure PowerShell nie gromadzi żadnych danych prywatnych ani żadnych informacji umożliwiających identyfikację użytkownika.</span><span class="sxs-lookup"><span data-stu-id="94f58-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="94f58-111">Uruchom polecenie cmdlet Disable-AzureRMDataCollection, aby wyłączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="94f58-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="94f58-112">Zapobiegnie to monitowaniu bieżącego użytkownika o zbieranie danych przy pierwszym uruchomieniu poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f58-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="94f58-113">Aby włączyć zbieranie danych dla bieżącego użytkownika, uruchom polecenie cmdlet Enable-AzureRmDataCollection.</span><span class="sxs-lookup"><span data-stu-id="94f58-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="94f58-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="94f58-114">EXAMPLES</span></span>

### <span data-ttu-id="94f58-115">Przykład 1: wyłączanie zbierania danych dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="94f58-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="94f58-116">W tym przykładzie pokazano, jak wyłączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="94f58-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="94f58-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="94f58-117">PARAMETERS</span></span>

### <span data-ttu-id="94f58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f58-118">-DefaultProfile</span></span>
<span data-ttu-id="94f58-119">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="94f58-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94f58-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="94f58-120">-Confirm</span></span>
<span data-ttu-id="94f58-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f58-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f58-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f58-122">-WhatIf</span></span>
<span data-ttu-id="94f58-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94f58-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94f58-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="94f58-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f58-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f58-125">CommonParameters</span></span>
<span data-ttu-id="94f58-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94f58-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f58-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94f58-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f58-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94f58-128">INPUTS</span></span>

## <span data-ttu-id="94f58-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="94f58-129">OUTPUTS</span></span>

### <span data-ttu-id="94f58-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="94f58-130">None</span></span>

## <span data-ttu-id="94f58-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="94f58-131">NOTES</span></span>

## <span data-ttu-id="94f58-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94f58-132">RELATED LINKS</span></span>

[<span data-ttu-id="94f58-133">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="94f58-133">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)

