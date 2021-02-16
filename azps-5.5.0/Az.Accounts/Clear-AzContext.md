---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/clear-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Clear-AzContext.md
ms.openlocfilehash: b808f9272c000ed0ef17079dd31800860a31449b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199938"
---
# <span data-ttu-id="fc70f-101">Clear-AzContext</span><span class="sxs-lookup"><span data-stu-id="fc70f-101">Clear-AzContext</span></span>

## <span data-ttu-id="fc70f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc70f-102">SYNOPSIS</span></span>
<span data-ttu-id="fc70f-103">Usuń wszystkie poświadczenia platformy Azure, konto i informacje o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fc70f-103">Remove all Azure credentials, account, and subscription information.</span></span>

## <span data-ttu-id="fc70f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fc70f-104">SYNTAX</span></span>

```
Clear-AzContext [-PassThru] [-Force] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc70f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fc70f-105">DESCRIPTION</span></span>
<span data-ttu-id="fc70f-106">Usuń wszystkie poświadczenia platformy Azure, konto i informacje o subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fc70f-106">Remove all Azure Credentials, account, and subscription information.</span></span>

## <span data-ttu-id="fc70f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fc70f-107">EXAMPLES</span></span>

### <span data-ttu-id="fc70f-108">Przykład 1. Wyczyść kontekst globalny</span><span class="sxs-lookup"><span data-stu-id="fc70f-108">Example 1: Clear global context</span></span>
```powershell
PS C:\> Clear-AzContext -Scope CurrentUser
```

<span data-ttu-id="fc70f-109">Usuń wszystkie informacje o koncie, subskrypcji i poświadczeniach dla dowolnej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc70f-109">Remove all account, subscription, and credential information for any powershell session.</span></span>

## <span data-ttu-id="fc70f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc70f-110">PARAMETERS</span></span>

### <span data-ttu-id="fc70f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc70f-111">-DefaultProfile</span></span>
<span data-ttu-id="fc70f-112">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fc70f-112">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc70f-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="fc70f-113">-Force</span></span>
<span data-ttu-id="fc70f-114">Usuwanie wszystkich użytkowników i grup z zakresu globalnego bez monitowania</span><span class="sxs-lookup"><span data-stu-id="fc70f-114">Delete all users and groups from the global scope without prompting</span></span>

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

### <span data-ttu-id="fc70f-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc70f-115">-PassThru</span></span>
<span data-ttu-id="fc70f-116">Zwraca wartość wskazującą sukces lub porażkę.</span><span class="sxs-lookup"><span data-stu-id="fc70f-116">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="fc70f-117">— Zakres</span><span class="sxs-lookup"><span data-stu-id="fc70f-117">-Scope</span></span>
<span data-ttu-id="fc70f-118">Wyczyść kontekst tylko dla bieżącej sesji programu PowerShell lub wszystkich sesji.</span><span class="sxs-lookup"><span data-stu-id="fc70f-118">Clear the context only for the current PowerShell session, or for all sessions.</span></span>

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

### <span data-ttu-id="fc70f-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc70f-119">-Confirm</span></span>
<span data-ttu-id="fc70f-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fc70f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc70f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc70f-121">-WhatIf</span></span>
<span data-ttu-id="fc70f-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc70f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc70f-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fc70f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc70f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc70f-124">CommonParameters</span></span>
<span data-ttu-id="fc70f-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc70f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc70f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc70f-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc70f-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc70f-127">INPUTS</span></span>

### <span data-ttu-id="fc70f-128">Brak</span><span class="sxs-lookup"><span data-stu-id="fc70f-128">None</span></span>

## <span data-ttu-id="fc70f-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc70f-129">OUTPUTS</span></span>

### <span data-ttu-id="fc70f-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fc70f-130">System.Boolean</span></span>

## <span data-ttu-id="fc70f-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fc70f-131">NOTES</span></span>

## <span data-ttu-id="fc70f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc70f-132">RELATED LINKS</span></span>
