---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/uninstall-azurerm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Uninstall-AzureRm.md
ms.openlocfilehash: 796690bd0a5774e488b978003c48b02eedaac190
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967089"
---
# <span data-ttu-id="0014e-101">Uninstall-AzureRm</span><span class="sxs-lookup"><span data-stu-id="0014e-101">Uninstall-AzureRm</span></span>

## <span data-ttu-id="0014e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0014e-102">SYNOPSIS</span></span>
<span data-ttu-id="0014e-103">Usuwa wszystkie moduły usługi AzureRm z komputera.</span><span class="sxs-lookup"><span data-stu-id="0014e-103">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="0014e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0014e-104">SYNTAX</span></span>

```
Uninstall-AzureRm [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0014e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="0014e-105">DESCRIPTION</span></span>
<span data-ttu-id="0014e-106">Usuwa wszystkie moduły usługi AzureRm z komputera.</span><span class="sxs-lookup"><span data-stu-id="0014e-106">Removes all AzureRm modules from a machine.</span></span>

## <span data-ttu-id="0014e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0014e-107">EXAMPLES</span></span>

### <span data-ttu-id="0014e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0014e-108">Example 1</span></span>
```
PS C:\> Uninstall-AzureRm
```

<span data-ttu-id="0014e-109">Uruchomienie tego polecenia spowoduje usunięcie z komputera wszystkich modułów usługi AzureRm dla wersji programu PowerShell, w której jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0014e-109">Running this command will remove all AzureRm modules from the machine for the version of PowerShell in which the cmdlet is run.</span></span>

## <span data-ttu-id="0014e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0014e-110">PARAMETERS</span></span>

### <span data-ttu-id="0014e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0014e-111">-DefaultProfile</span></span>
<span data-ttu-id="0014e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="0014e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0014e-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0014e-113">-PassThru</span></span>
<span data-ttu-id="0014e-114">Lista zwracanych modułów usunięta, jeśli została określona.</span><span class="sxs-lookup"><span data-stu-id="0014e-114">Return list of Modules removed if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0014e-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0014e-115">-Confirm</span></span>
<span data-ttu-id="0014e-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0014e-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0014e-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0014e-117">-WhatIf</span></span>
<span data-ttu-id="0014e-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0014e-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0014e-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0014e-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0014e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0014e-120">CommonParameters</span></span>
<span data-ttu-id="0014e-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0014e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0014e-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0014e-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0014e-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0014e-123">INPUTS</span></span>

### <span data-ttu-id="0014e-124">Brak</span><span class="sxs-lookup"><span data-stu-id="0014e-124">None</span></span>

## <span data-ttu-id="0014e-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0014e-125">OUTPUTS</span></span>

### <span data-ttu-id="0014e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="0014e-126">System.String</span></span>

## <span data-ttu-id="0014e-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0014e-127">NOTES</span></span>

## <span data-ttu-id="0014e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0014e-128">RELATED LINKS</span></span>
