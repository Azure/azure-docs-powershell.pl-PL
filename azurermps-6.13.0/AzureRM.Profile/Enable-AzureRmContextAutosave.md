---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmContextAutosave.md
ms.openlocfilehash: ef36772679cb6d34ad469c6d78550634e6dec954
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719066"
---
# <span data-ttu-id="6fccf-101">Enable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="6fccf-101">Enable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="6fccf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fccf-102">SYNOPSIS</span></span>
<span data-ttu-id="6fccf-103">Zezwalaj na zapisywanie i automatyczne ładowanie informacji o poświadczeniach platformy Azure, kontach i subskrypcjach podczas otwierania okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6fccf-103">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fccf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fccf-104">SYNTAX</span></span>

```
Enable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fccf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6fccf-105">DESCRIPTION</span></span>
<span data-ttu-id="6fccf-106">Zezwalaj na zapisywanie i automatyczne ładowanie informacji o poświadczeniach platformy Azure, kontach i subskrypcjach podczas otwierania okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6fccf-106">Allow the azure credential, account and subscription information to be saved and automatically loaded when you open a PowerShell window.</span></span> 

## <span data-ttu-id="6fccf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fccf-107">EXAMPLES</span></span>

### <span data-ttu-id="6fccf-108">Włączanie autozapisywania poświadczeń dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="6fccf-108">Enable autosaving credentials for the current user</span></span>
```
PS C:\> Enable-AzureRmContextAutosave
```

<span data-ttu-id="6fccf-109">Włącz funkcję Autozapisu w poświadczeniach dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6fccf-109">Turn on credential autosave for the current user.</span></span>  <span data-ttu-id="6fccf-110">Za każdym razem, gdy zostanie otwarte okno programu PowerShell, Twój bieżący kontekst zostanie zapamiętany bez logowania.</span><span class="sxs-lookup"><span data-stu-id="6fccf-110">Whenever a powershell window is opened, your current context will be remembered without logging in.</span></span>

## <span data-ttu-id="6fccf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fccf-111">PARAMETERS</span></span>

### <span data-ttu-id="6fccf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fccf-112">-DefaultProfile</span></span>
<span data-ttu-id="6fccf-113">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6fccf-113">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fccf-114">-Zakres</span><span class="sxs-lookup"><span data-stu-id="6fccf-114">-Scope</span></span>
<span data-ttu-id="6fccf-115">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6fccf-115">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="6fccf-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fccf-116">-Confirm</span></span>
<span data-ttu-id="6fccf-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fccf-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fccf-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fccf-118">-WhatIf</span></span>
<span data-ttu-id="6fccf-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fccf-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fccf-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6fccf-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fccf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fccf-121">CommonParameters</span></span>
<span data-ttu-id="6fccf-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fccf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fccf-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fccf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fccf-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fccf-124">INPUTS</span></span>

### <span data-ttu-id="6fccf-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6fccf-125">None</span></span>

## <span data-ttu-id="6fccf-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fccf-126">OUTPUTS</span></span>

### <span data-ttu-id="6fccf-127">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="6fccf-127">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="6fccf-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fccf-128">NOTES</span></span>

## <span data-ttu-id="6fccf-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fccf-129">RELATED LINKS</span></span>