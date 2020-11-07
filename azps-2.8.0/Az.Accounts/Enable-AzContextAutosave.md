---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: eedd28fe1df7992658dfe9b36ebab58e77eb87c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707232"
---
# <span data-ttu-id="96cd4-101">Enable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="96cd4-101">Enable-AzContextAutosave</span></span>

## <span data-ttu-id="96cd4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96cd4-102">SYNOPSIS</span></span>
<span data-ttu-id="96cd4-103">Zezwalaj na zapisywanie i automatyczne ładowanie informacji o poświadczeniach platformy Azure, kontach i subskrypcjach podczas otwierania okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="96cd4-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="96cd4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96cd4-104">SYNTAX</span></span>

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96cd4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="96cd4-105">DESCRIPTION</span></span>
<span data-ttu-id="96cd4-106">Zezwalaj na zapisywanie i automatyczne ładowanie informacji o poświadczeniach platformy Azure, kontach i subskrypcjach podczas otwierania okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="96cd4-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="96cd4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96cd4-107">EXAMPLES</span></span>

### <span data-ttu-id="96cd4-108">Włączanie autozapisywania poświadczeń dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="96cd4-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzContextAutosave
```

<span data-ttu-id="96cd4-109">Włącz funkcję Autozapisu w poświadczeniach dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="96cd4-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="96cd4-110">Za każdym razem, gdy zostanie otwarte okno programu PowerShell, Twój bieżący kontekst zostanie zapamiętany bez logowania.</span><span class="sxs-lookup"><span data-stu-id="96cd4-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="96cd4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96cd4-111">PARAMETERS</span></span>

### <span data-ttu-id="96cd4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96cd4-112">-DefaultProfile</span></span>
<span data-ttu-id="96cd4-113">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="96cd4-113">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96cd4-114">-Zakres</span><span class="sxs-lookup"><span data-stu-id="96cd4-114">-Scope</span></span>
<span data-ttu-id="96cd4-115">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="96cd4-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="96cd4-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96cd4-116">-Confirm</span></span>
<span data-ttu-id="96cd4-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96cd4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96cd4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96cd4-118">-WhatIf</span></span>
<span data-ttu-id="96cd4-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96cd4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96cd4-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="96cd4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96cd4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cd4-121">CommonParameters</span></span>
<span data-ttu-id="96cd4-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96cd4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cd4-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96cd4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cd4-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96cd4-124">INPUTS</span></span>

### <span data-ttu-id="96cd4-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="96cd4-125">None</span></span>

## <span data-ttu-id="96cd4-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96cd4-126">OUTPUTS</span></span>

### <span data-ttu-id="96cd4-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="96cd4-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="96cd4-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96cd4-128">NOTES</span></span>

## <span data-ttu-id="96cd4-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96cd4-129">RELATED LINKS</span></span>
