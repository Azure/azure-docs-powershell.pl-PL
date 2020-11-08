---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/rename-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Rename-AzContext.md
ms.openlocfilehash: 09c0faec1ab424ef1bfb10fec35dd59646e4711c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220877"
---
# <span data-ttu-id="d57d9-101">Rename-AzContext</span><span class="sxs-lookup"><span data-stu-id="d57d9-101">Rename-AzContext</span></span>

## <span data-ttu-id="d57d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d57d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d57d9-103">Zmienianie nazwy kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d57d9-103">Rename an Azure context.</span></span>  <span data-ttu-id="d57d9-104">Domyślnie nazwy kontekstowe są nazywane przez konto użytkownika i abonament.</span><span class="sxs-lookup"><span data-stu-id="d57d9-104">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="d57d9-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d57d9-105">SYNTAX</span></span>

### <span data-ttu-id="d57d9-106">RenameByInputObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d57d9-106">RenameByInputObject (Default)</span></span>
```
Rename-AzContext -InputObject <PSAzureContext> [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-TargetName] <String> [<CommonParameters>]
```

### <span data-ttu-id="d57d9-107">RenameByName</span><span class="sxs-lookup"><span data-stu-id="d57d9-107">RenameByName</span></span>
```
Rename-AzContext [-Force] [-PassThru] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [-SourceName] <String> [-TargetName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="d57d9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d57d9-108">DESCRIPTION</span></span>
<span data-ttu-id="d57d9-109">Zmienianie nazwy kontekstu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d57d9-109">Rename an Azure context.</span></span>  <span data-ttu-id="d57d9-110">Domyślnie nazwy kontekstowe są nazywane przez konto użytkownika i abonament.</span><span class="sxs-lookup"><span data-stu-id="d57d9-110">By default contexts are named by user account and subscription.</span></span>

## <span data-ttu-id="d57d9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d57d9-111">EXAMPLES</span></span>

### <span data-ttu-id="d57d9-112">Przykład 1: Zmienianie nazwy kontekstu przy użyciu nazwanych parametrów</span><span class="sxs-lookup"><span data-stu-id="d57d9-112">Example 1: Rename a context using named parameters</span></span>
```powershell
PS C:\> Rename-AzContext -SourceName "[user1@contoso.org; 12345-6789-2345-3567890]" -TargetName "Work"
```

<span data-ttu-id="d57d9-113">Zmień nazwę kontekstu dla user1@contoso.org subskrypcji "12345-6789-2345-3567890" na "praca".</span><span class="sxs-lookup"><span data-stu-id="d57d9-113">Rename the context for 'user1@contoso.org' with subscription '12345-6789-2345-3567890' to 'Work'.</span></span>  <span data-ttu-id="d57d9-114">Po wykonaniu tego polecenia będziesz mieć możliwość kierowania kontekstu przy użyciu funkcji "Select-AzContext Work".</span><span class="sxs-lookup"><span data-stu-id="d57d9-114">After this command, you will be able to target the context using 'Select-AzContext Work'.</span></span>  <span data-ttu-id="d57d9-115">Zwróć uwagę, że możesz przełączać się między wartościami "SourceName" przy użyciu funkcji kończenia karty.</span><span class="sxs-lookup"><span data-stu-id="d57d9-115">Note that you can tab through the values for 'SourceName' using tab completion.</span></span>

### <span data-ttu-id="d57d9-116">Przykład 2: Zmienianie nazwy kontekstu przy użyciu parametrów pozycyjnych</span><span class="sxs-lookup"><span data-stu-id="d57d9-116">Example 2: Rename a context using positional parameters</span></span>
```powershell
PS C:\> Rename-AzContext "My context" "Work"
```

<span data-ttu-id="d57d9-117">Zmień nazwę kontekstu o nazwie "mój kontekst" na "praca".</span><span class="sxs-lookup"><span data-stu-id="d57d9-117">Rename the context named "My context" to "Work".</span></span>  <span data-ttu-id="d57d9-118">Po tym poleceniu będziesz mieć możliwość kierowania kontekstu przy użyciu Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="d57d9-118">After this command, you will be able to target the context using Select-AzContext Work</span></span>

## <span data-ttu-id="d57d9-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d57d9-119">PARAMETERS</span></span>

### <span data-ttu-id="d57d9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57d9-120">-DefaultProfile</span></span>
<span data-ttu-id="d57d9-121">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d57d9-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d57d9-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d57d9-122">-Force</span></span>
<span data-ttu-id="d57d9-123">Zmienianie nazwy kontekstu, nawet jeśli kontekst docelowy już istnieje</span><span class="sxs-lookup"><span data-stu-id="d57d9-123">Rename the context even if the target context already exists</span></span>

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

### <span data-ttu-id="d57d9-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d57d9-124">-InputObject</span></span>
<span data-ttu-id="d57d9-125">Obiekt kontekstu, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="d57d9-125">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: RenameByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d57d9-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d57d9-126">-PassThru</span></span>
<span data-ttu-id="d57d9-127">Zwraca kontekst o zmienionej nazwie.</span><span class="sxs-lookup"><span data-stu-id="d57d9-127">Return the renamed context.</span></span>

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

### <span data-ttu-id="d57d9-128">-Zakres</span><span class="sxs-lookup"><span data-stu-id="d57d9-128">-Scope</span></span>
<span data-ttu-id="d57d9-129">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d57d9-129">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="d57d9-130">-SourceName</span><span class="sxs-lookup"><span data-stu-id="d57d9-130">-SourceName</span></span>
<span data-ttu-id="d57d9-131">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="d57d9-131">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: RenameByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57d9-132">-TargetName</span><span class="sxs-lookup"><span data-stu-id="d57d9-132">-TargetName</span></span>
<span data-ttu-id="d57d9-133">Nowa nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="d57d9-133">The new name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d57d9-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d57d9-134">-Confirm</span></span>
<span data-ttu-id="d57d9-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d57d9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d57d9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d57d9-136">-WhatIf</span></span>
<span data-ttu-id="d57d9-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d57d9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d57d9-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d57d9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d57d9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57d9-139">CommonParameters</span></span>
<span data-ttu-id="d57d9-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d57d9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d57d9-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57d9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57d9-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d57d9-142">INPUTS</span></span>

### <span data-ttu-id="d57d9-143">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d57d9-143">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="d57d9-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d57d9-144">OUTPUTS</span></span>

### <span data-ttu-id="d57d9-145">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d57d9-145">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="d57d9-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d57d9-146">NOTES</span></span>

## <span data-ttu-id="d57d9-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d57d9-147">RELATED LINKS</span></span>
