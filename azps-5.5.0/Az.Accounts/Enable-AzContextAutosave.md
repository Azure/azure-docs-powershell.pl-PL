---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195443"
---
# <span data-ttu-id="e9a19-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="e9a19-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="e9a19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9a19-102">SYNOPSIS</span></span>
<span data-ttu-id="e9a19-103">Konteksty platformy Azure to obiekty programu PowerShell reprezentujące aktywną subskrypcję, dla których mają być uruchamiane polecenia, oraz informacje o uwierzytelnianiu potrzebne do nawiązania połączenia z chmurą platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e9a19-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="e9a19-104">W kontekście platformy Azure program Azure PowerShell nie musi ponownie uwierzytelniania konta przy każdym przełączaniu subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e9a19-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="e9a19-105">Aby uzyskać więcej informacji, zobacz [obiekty kontekstowe programu Azure PowerShell.](https://docs.microsoft.com/powershell/azure/context-persistence)</span><span class="sxs-lookup"><span data-stu-id="e9a19-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="e9a19-106">To polecenie cmdlet umożliwia zapisanie i automatyczne załadowanie informacji kontekstowych platformy Azure po uruchomieniu procesu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e9a19-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="e9a19-107">Na przykład podczas otwierania nowego okna.</span><span class="sxs-lookup"><span data-stu-id="e9a19-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="e9a19-108">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e9a19-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9a19-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="e9a19-109">DESCRIPTION</span></span>

<span data-ttu-id="e9a19-110">Umożliwia zapisanie i automatyczne załadowanie informacji kontekstowych platformy Azure podczas uruchamiania procesu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e9a19-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="e9a19-111">Kontekst jest zapisywany na końcu wykonywania każdego polecenia cmdlet mającego wpływ na kontekst.</span><span class="sxs-lookup"><span data-stu-id="e9a19-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="e9a19-112">Na przykład dowolne polecenie cmdlet profilu.</span><span class="sxs-lookup"><span data-stu-id="e9a19-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="e9a19-113">Jeśli korzystasz z uwierzytelniania użytkownika, tokeny mogą być aktualizowane w trakcie uruchamiania dowolnego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9a19-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="e9a19-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e9a19-114">EXAMPLES</span></span>

### <span data-ttu-id="e9a19-115">Przykład 1. Włączanie poświadczeń automatycznegoavingu dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="e9a19-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="e9a19-116">Włącz funkcję autozazysowania poświadczeń dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e9a19-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="e9a19-117">Przy każdym otwarciu okna programu PowerShell zostanie zapamiętany bieżący kontekst bez logowania się.</span><span class="sxs-lookup"><span data-stu-id="e9a19-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="e9a19-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e9a19-118">Example 2</span></span>

<span data-ttu-id="e9a19-119">Zezwalaj na zapisanie i automatyczne załadowanie poświadczeń, konta i subskrypcji platformy Azure po otwarciu okna programu PowerShell w tej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e9a19-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="e9a19-120">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="e9a19-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="e9a19-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9a19-121">PARAMETERS</span></span>

### <span data-ttu-id="e9a19-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9a19-122">-DefaultProfile</span></span>

<span data-ttu-id="e9a19-123">Poświadczenia, dzierżawy i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e9a19-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="e9a19-124">— Zakres</span><span class="sxs-lookup"><span data-stu-id="e9a19-124">-Scope</span></span>

<span data-ttu-id="e9a19-125">Określa zakres zmian kontekstu.</span><span class="sxs-lookup"><span data-stu-id="e9a19-125">Determines the scope of context changes.</span></span> <span data-ttu-id="e9a19-126">Może to być na przykład zmiana mająca zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e9a19-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="e9a19-127">Zmiany wprowadzone w zakresie mają `CurrentUser` wpływ na wszystkie sesje programu PowerShell rozpoczęte przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e9a19-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="e9a19-128">Jeśli dla określonej sesji są potrzebne różne ustawienia, należy użyć `Process` zakresu.</span><span class="sxs-lookup"><span data-stu-id="e9a19-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9a19-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9a19-129">-Confirm</span></span>

<span data-ttu-id="e9a19-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e9a19-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9a19-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9a19-131">-WhatIf</span></span>

<span data-ttu-id="e9a19-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9a19-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9a19-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e9a19-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="e9a19-134">Typowe parametry</span><span class="sxs-lookup"><span data-stu-id="e9a19-134">Common Parameters</span></span>

<span data-ttu-id="e9a19-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9a19-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9a19-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e9a19-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9a19-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9a19-137">INPUTS</span></span>

### <span data-ttu-id="e9a19-138">Brak</span><span class="sxs-lookup"><span data-stu-id="e9a19-138">None</span></span>

## <span data-ttu-id="e9a19-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9a19-139">OUTPUTS</span></span>

### <span data-ttu-id="e9a19-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="e9a19-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="e9a19-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e9a19-141">NOTES</span></span>

## <span data-ttu-id="e9a19-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9a19-142">RELATED LINKS</span></span>
