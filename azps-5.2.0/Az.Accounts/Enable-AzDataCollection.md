---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: a8087f41c33dc3bb066609393a87986d5016d1ae
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333214"
---
# <span data-ttu-id="8cf16-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="8cf16-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="8cf16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cf16-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf16-103">Umożliwia zbieranie danych w celu usprawnienia środowiska użytkownika za pomocą poleceń cmdlet środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cf16-103">Enables Azure PowerShell to collect data to improve the user experience with the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="8cf16-104">Wykonanie tego polecenia cmdlet umożliwia zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="8cf16-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span> <span data-ttu-id="8cf16-105">Dane są zbierane domyślnie, o ile użytkownik wyraźnie nie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="8cf16-105">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="8cf16-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cf16-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf16-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8cf16-107">DESCRIPTION</span></span>

<span data-ttu-id="8cf16-108">Za pomocą polecenia cmdlet można dołączać `Enable-AzDataCollection` do kolekcji danych.</span><span class="sxs-lookup"><span data-stu-id="8cf16-108">The `Enable-AzDataCollection` cmdlet is used to opt in to data collection.</span></span> <span data-ttu-id="8cf16-109">Program Azure PowerShell domyślnie automatycznie zbiera dane telemetryczne.</span><span class="sxs-lookup"><span data-stu-id="8cf16-109">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="8cf16-110">Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania, identyfikowania typowych problemów oraz usprawnienia środowiska usługi Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8cf16-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span>
<span data-ttu-id="8cf16-111">Program Microsoft Azure PowerShell nie gromadzi danych prywatnych ani osobistych.</span><span class="sxs-lookup"><span data-stu-id="8cf16-111">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="8cf16-112">Aby wyłączyć zbieranie danych, należy wyraźnie zrezygnować z wykonywania `Disable-AzDataCollection` .</span><span class="sxs-lookup"><span data-stu-id="8cf16-112">To disable data collection, you must explicitly opt out by executing `Disable-AzDataCollection`.</span></span>

## <span data-ttu-id="8cf16-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cf16-113">EXAMPLES</span></span>

### <span data-ttu-id="8cf16-114">Przykład 1: Włączanie zbierania danych dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="8cf16-114">Example 1: Enabling data collection for the current user</span></span>

<span data-ttu-id="8cf16-115">W poniższym przykładzie pokazano, jak włączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8cf16-115">The following example shows how to enable data collection for the current user.</span></span>

```powershell
Enable-AzDataCollection
```

## <span data-ttu-id="8cf16-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cf16-116">PARAMETERS</span></span>

### <span data-ttu-id="8cf16-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf16-117">-DefaultProfile</span></span>

<span data-ttu-id="8cf16-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf16-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cf16-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8cf16-119">-Confirm</span></span>

<span data-ttu-id="8cf16-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf16-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf16-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf16-121">-WhatIf</span></span>

<span data-ttu-id="8cf16-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf16-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cf16-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8cf16-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf16-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf16-124">CommonParameters</span></span>

<span data-ttu-id="8cf16-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf16-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf16-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="8cf16-126">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="8cf16-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cf16-127">INPUTS</span></span>

### <span data-ttu-id="8cf16-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8cf16-128">None</span></span>

## <span data-ttu-id="8cf16-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cf16-129">OUTPUTS</span></span>

### <span data-ttu-id="8cf16-130">System. void</span><span class="sxs-lookup"><span data-stu-id="8cf16-130">System.Void</span></span>

## <span data-ttu-id="8cf16-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cf16-131">NOTES</span></span>

## <span data-ttu-id="8cf16-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cf16-132">RELATED LINKS</span></span>

[<span data-ttu-id="8cf16-133">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="8cf16-133">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)
