---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/30/2020
ms.locfileid: "94054046"
---
# <span data-ttu-id="3046e-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="3046e-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="3046e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3046e-102">SYNOPSIS</span></span>
<span data-ttu-id="3046e-103">Zrezygnowano z gromadzenia danych w celu ulepszenia poleceń cmdlet programu PowerShell w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="3046e-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="3046e-104">Dane są zbierane domyślnie, o ile użytkownik wyraźnie nie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="3046e-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="3046e-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3046e-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3046e-106">Opis</span><span class="sxs-lookup"><span data-stu-id="3046e-106">DESCRIPTION</span></span>

<span data-ttu-id="3046e-107">`Disable-AzDataCollection`Polecenie cmdlet umożliwia rezygnację z zbierania danych.</span><span class="sxs-lookup"><span data-stu-id="3046e-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="3046e-108">Program Azure PowerShell domyślnie automatycznie zbiera dane telemetryczne.</span><span class="sxs-lookup"><span data-stu-id="3046e-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="3046e-109">Aby wyłączyć zbieranie danych, musisz wyraźnie zrezygnować. Firma Microsoft gromadzi zebrane dane w celu zidentyfikowania wzorców użytkowania, identyfikowania typowych problemów oraz usprawnienia środowiska usługi Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3046e-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="3046e-110">Program Microsoft Azure PowerShell nie gromadzi danych prywatnych ani osobistych.</span><span class="sxs-lookup"><span data-stu-id="3046e-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="3046e-111">Jeśli wcześniej wybrałeś opcję, uruchom `Enable-AzDataCollection` polecenie cmdlet, aby ponownie włączyć zbieranie danych dla bieżącego użytkownika na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="3046e-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="3046e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3046e-112">EXAMPLES</span></span>

### <span data-ttu-id="3046e-113">Przykład 1: wyłączanie zbierania danych dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="3046e-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="3046e-114">W poniższym przykładzie pokazano, jak wyłączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3046e-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="3046e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3046e-115">PARAMETERS</span></span>

### <span data-ttu-id="3046e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3046e-116">-DefaultProfile</span></span>

<span data-ttu-id="3046e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3046e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3046e-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3046e-118">-Confirm</span></span>

<span data-ttu-id="3046e-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3046e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3046e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3046e-120">-WhatIf</span></span>

<span data-ttu-id="3046e-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3046e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3046e-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3046e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3046e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3046e-123">CommonParameters</span></span>

<span data-ttu-id="3046e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3046e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3046e-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="3046e-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="3046e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3046e-126">INPUTS</span></span>

### <span data-ttu-id="3046e-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3046e-127">None</span></span>

## <span data-ttu-id="3046e-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3046e-128">OUTPUTS</span></span>

### <span data-ttu-id="3046e-129">System. void</span><span class="sxs-lookup"><span data-stu-id="3046e-129">System.Void</span></span>

## <span data-ttu-id="3046e-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3046e-130">NOTES</span></span>

## <span data-ttu-id="3046e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3046e-131">RELATED LINKS</span></span>

[<span data-ttu-id="3046e-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="3046e-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
