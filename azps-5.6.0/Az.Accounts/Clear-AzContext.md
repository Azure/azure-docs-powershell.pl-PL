---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: 8db930fe362d25a7b1069af6c3855ef71644e874
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990627"
---
# <span data-ttu-id="36a31-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="36a31-101">Clear-AzContext</span></span>

## <span data-ttu-id="36a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36a31-102">SYNOPSIS</span></span>
<span data-ttu-id="36a31-103">Usuń wszystkie poświadczenia platformy Azure, konto i informacje o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="36a31-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="36a31-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="36a31-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36a31-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="36a31-105">DESCRIPTION</span></span>
<span data-ttu-id="36a31-106">Usuń wszystkie poświadczenia platformy Azure, konto i informacje o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="36a31-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="36a31-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="36a31-107">EXAMPLES</span></span>

### <span data-ttu-id="36a31-108">Przykład 1. Wyczyść kontekst globalny</span><span class="sxs-lookup"><span data-stu-id="36a31-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="36a31-109">Usuń wszystkie informacje o koncie, subskrypcji i poświadczeniach dla dowolnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="36a31-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="36a31-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36a31-110">PARAMETERS</span></span>

### <span data-ttu-id="36a31-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36a31-111">-DefaultProfile</span></span>
<span data-ttu-id="36a31-112">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="36a31-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36a31-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="36a31-113">-Force</span></span>
<span data-ttu-id="36a31-114">Usuwanie wszystkich użytkowników i grup z zakresu globalnego bez monitowania</span><span class="sxs-lookup"><span data-stu-id="36a31-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="36a31-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36a31-115">-PassThru</span></span>
<span data-ttu-id="36a31-116">Zwraca wartość wskazującą sukces lub porażkę.</span><span class="sxs-lookup"><span data-stu-id="36a31-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="36a31-117">— Zakres</span><span class="sxs-lookup"><span data-stu-id="36a31-117">-Scope</span></span>
<span data-ttu-id="36a31-118">Wyczyść kontekst tylko dla bieżącej sesji programu PowerShell lub wszystkich sesji.</span><span class="sxs-lookup"><span data-stu-id="36a31-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36a31-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36a31-119">-Confirm</span></span>
<span data-ttu-id="36a31-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36a31-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36a31-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36a31-121">-WhatIf</span></span>
<span data-ttu-id="36a31-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36a31-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36a31-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="36a31-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36a31-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36a31-124">CommonParameters</span></span>
<span data-ttu-id="36a31-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36a31-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36a31-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36a31-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36a31-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36a31-127">INPUTS</span></span>

### <span data-ttu-id="36a31-128">Brak</span><span class="sxs-lookup"><span data-stu-id="36a31-128">None</span></span>

## <span data-ttu-id="36a31-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36a31-129">OUTPUTS</span></span>

### <span data-ttu-id="36a31-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36a31-130">System.Boolean</span></span>

## <span data-ttu-id="36a31-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="36a31-131">NOTES</span></span>

## <span data-ttu-id="36a31-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36a31-132">RELATED LINKS</span></span>
