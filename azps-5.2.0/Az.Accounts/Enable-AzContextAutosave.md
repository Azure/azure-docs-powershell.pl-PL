---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370876"
---
# <span data-ttu-id="2a7ac-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="2a7ac-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="2a7ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a7ac-102">SYNOPSIS</span></span>
<span data-ttu-id="2a7ac-103">Konteksty platformy Azure to obiekty programu PowerShell reprezentujące aktywną subskrypcję, za pomocą których można uruchamiać polecenia, oraz informacje uwierzytelniające potrzebne do nawiązania połączenia z chmurą platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-103">Azure contexts are PowerShell objects representing your active subscription to run commands against, and the authentication information needed to connect to an Azure cloud.</span></span> <span data-ttu-id="2a7ac-104">W przypadku kontekstów platformy Azure Program Azure PowerShell nie musi ponownie uwierzytelniać konta za każdym razem, gdy użytkownik przełączy abonament.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-104">With Azure contexts, Azure PowerShell doesn't need to reauthenticate your account each time you switch subscriptions.</span></span> <span data-ttu-id="2a7ac-105">Aby uzyskać więcej informacji, zobacz [obiekty kontekstu środowiska Azure PowerShell](https://docs.microsoft.com/powershell/azure/context-persistence).</span><span class="sxs-lookup"><span data-stu-id="2a7ac-105">For more information, see [Azure PowerShell context objects](https://docs.microsoft.com/powershell/azure/context-persistence).</span></span>

<span data-ttu-id="2a7ac-106">To polecenie cmdlet umożliwia zapisywanie i automatyczne ładowanie informacji kontekstowych platformy Azure po uruchomieniu procesu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-106">This cmdlet allows the Azure context information to be saved and automatically loaded when you start a PowerShell process.</span></span> <span data-ttu-id="2a7ac-107">Na przykład podczas otwierania nowego okna.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-107">For example, when opening a new window.</span></span>

## <span data-ttu-id="2a7ac-108">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a7ac-108">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a7ac-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2a7ac-109">DESCRIPTION</span></span>

<span data-ttu-id="2a7ac-110">Umożliwia zapisywanie i automatyczne ładowanie informacji o kontekście platformy Azure po uruchomieniu procesu programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-110">Allows the Azure context information to be saved and automatically loaded when a PowerShell process starts.</span></span> <span data-ttu-id="2a7ac-111">Kontekst zostanie zapisany na końcu wykonania dowolnego polecenia cmdlet, które wpływa na kontekst.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-111">The context is saved at the end of the execution of any cmdlet that affects the context.</span></span> <span data-ttu-id="2a7ac-112">Na przykład dowolne polecenie cmdlet profile.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-112">For example, any profile cmdlet.</span></span> <span data-ttu-id="2a7ac-113">Jeśli korzystasz z uwierzytelniania użytkowników, tokeny mogą być aktualizowane w trakcie uruchamiania dowolnego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-113">If you're using user authentication, then tokens can be updated during the course of running any cmdlet.</span></span>

## <span data-ttu-id="2a7ac-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a7ac-114">EXAMPLES</span></span>

### <span data-ttu-id="2a7ac-115">Przykład 1: Włączanie autozapisywania poświadczeń dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="2a7ac-115">Example 1: Enable autosaving credentials for the current user</span></span>

<span data-ttu-id="2a7ac-116">Włącz funkcję Autozapisu w poświadczeniach dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-116">Turn on credential autosave for the current user.</span></span> <span data-ttu-id="2a7ac-117">Za każdym razem, gdy zostanie otwarte okno programu PowerShell, Twój bieżący kontekst zostanie zapamiętany bez logowania.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-117">Whenever a PowerShell window is opened, your current context is remembered without logging in.</span></span>

```powershell
Enable-AzContextAutosave
```

### <span data-ttu-id="2a7ac-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2a7ac-118">Example 2</span></span>

<span data-ttu-id="2a7ac-119">Zezwalanie na zapisywanie i automatyczne ładowanie informacji o poświadczeniach, kontach i subskrypcjach platformy Azure podczas otwierania okna programu PowerShell w tej sesji programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-119">Allow the Azure credential, account, and subscription information, to be saved and automatically loaded when you open a PowerShell window in this PowerShell session.</span></span> <span data-ttu-id="2a7ac-120">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="2a7ac-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## <span data-ttu-id="2a7ac-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a7ac-121">PARAMETERS</span></span>

### <span data-ttu-id="2a7ac-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a7ac-122">-DefaultProfile</span></span>

<span data-ttu-id="2a7ac-123">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2a7ac-123">The credentials, tenant, and subscription used for communication with Azure</span></span>

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

### <span data-ttu-id="2a7ac-124">-Zakres</span><span class="sxs-lookup"><span data-stu-id="2a7ac-124">-Scope</span></span>

<span data-ttu-id="2a7ac-125">Określa zakres zmian kontekstu.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-125">Determines the scope of context changes.</span></span> <span data-ttu-id="2a7ac-126">Na przykład, czy zmiany dotyczą tylko bieżącego procesu, czy wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-126">For example, whether changes apply only to the current process, or to all sessions started by this user.</span></span> <span data-ttu-id="2a7ac-127">Zmiany wprowadzone w zakresie wpłyną `CurrentUser` na wszystkie sesje programu PowerShell uruchomione przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-127">Changes made with the scope `CurrentUser` will affect all PowerShell sessions started by the user.</span></span> <span data-ttu-id="2a7ac-128">Jeśli określona sesja wymaga różnych ustawień, użyj zakresu `Process` .</span><span class="sxs-lookup"><span data-stu-id="2a7ac-128">If a particular session needs to have different settings, use the scope `Process`.</span></span>

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

### <span data-ttu-id="2a7ac-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2a7ac-129">-Confirm</span></span>

<span data-ttu-id="2a7ac-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a7ac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a7ac-131">-WhatIf</span></span>

<span data-ttu-id="2a7ac-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a7ac-133">Nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-133">The cmdlet isn't run.</span></span>

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

### <span data-ttu-id="2a7ac-134">Typowe parametry</span><span class="sxs-lookup"><span data-stu-id="2a7ac-134">Common Parameters</span></span>

<span data-ttu-id="2a7ac-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a7ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a7ac-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a7ac-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a7ac-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a7ac-137">INPUTS</span></span>

### <span data-ttu-id="2a7ac-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2a7ac-138">None</span></span>

## <span data-ttu-id="2a7ac-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a7ac-139">OUTPUTS</span></span>

### <span data-ttu-id="2a7ac-140">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="2a7ac-140">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="2a7ac-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a7ac-141">NOTES</span></span>

## <span data-ttu-id="2a7ac-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a7ac-142">RELATED LINKS</span></span>
