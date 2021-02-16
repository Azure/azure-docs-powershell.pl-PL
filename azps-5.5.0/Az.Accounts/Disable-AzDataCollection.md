---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195458"
---
# <span data-ttu-id="30ef1-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="30ef1-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="30ef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="30ef1-103">Zrezygnowano z gromadzenia danych w celu ulepszania poleceń cmdlet programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30ef1-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="30ef1-104">Dane są zbierane domyślnie, chyba że użytkownik jawnie zrezygnuje.</span><span class="sxs-lookup"><span data-stu-id="30ef1-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="30ef1-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="30ef1-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30ef1-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="30ef1-106">DESCRIPTION</span></span>

<span data-ttu-id="30ef1-107">Polecenie `Disable-AzDataCollection` cmdlet służy do rezygnacji z z gromadzenia danych.</span><span class="sxs-lookup"><span data-stu-id="30ef1-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="30ef1-108">Program Azure PowerShell domyślnie automatycznie zbiera dane telemetryczne.</span><span class="sxs-lookup"><span data-stu-id="30ef1-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="30ef1-109">Aby wyłączyć zbieranie danych, musisz jawnie zrezygnować. Firma Microsoft agreguje zebrane dane w celu identyfikowania wzorców użycia, identyfikowania typowych problemów i ulepszania środowiska programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="30ef1-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="30ef1-110">Program Microsoft Azure PowerShell nie zbiera żadnych prywatnych ani osobistych danych.</span><span class="sxs-lookup"><span data-stu-id="30ef1-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="30ef1-111">Jeśli wcześniej zrezygnowałeś(-aś), uruchom polecenie cmdlet, aby ponownie włączyć zbieranie danych dla bieżącego użytkownika `Enable-AzDataCollection` na bieżącym komputerze.</span><span class="sxs-lookup"><span data-stu-id="30ef1-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="30ef1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="30ef1-112">EXAMPLES</span></span>

### <span data-ttu-id="30ef1-113">Przykład 1. Wyłączanie zbierania danych dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="30ef1-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="30ef1-114">W poniższym przykładzie pokazano, jak wyłączyć zbieranie danych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="30ef1-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="30ef1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="30ef1-115">PARAMETERS</span></span>

### <span data-ttu-id="30ef1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ef1-116">-DefaultProfile</span></span>

<span data-ttu-id="30ef1-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="30ef1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30ef1-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30ef1-118">-Confirm</span></span>

<span data-ttu-id="30ef1-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="30ef1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30ef1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30ef1-120">-WhatIf</span></span>

<span data-ttu-id="30ef1-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30ef1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="30ef1-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="30ef1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30ef1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ef1-123">CommonParameters</span></span>

<span data-ttu-id="30ef1-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ef1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ef1-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="30ef1-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="30ef1-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30ef1-126">INPUTS</span></span>

### <span data-ttu-id="30ef1-127">Brak</span><span class="sxs-lookup"><span data-stu-id="30ef1-127">None</span></span>

## <span data-ttu-id="30ef1-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30ef1-128">OUTPUTS</span></span>

### <span data-ttu-id="30ef1-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="30ef1-129">System.Void</span></span>

## <span data-ttu-id="30ef1-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="30ef1-130">NOTES</span></span>

## <span data-ttu-id="30ef1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30ef1-131">RELATED LINKS</span></span>

[<span data-ttu-id="30ef1-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="30ef1-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)
