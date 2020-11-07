---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzContextAutosave.md
ms.openlocfilehash: 2147fd87cae8ef87010c54ce42dc33c85a8f6374
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704784"
---
# <span data-ttu-id="4cc10-101">Disable-AzContextAutosave</span><span class="sxs-lookup"><span data-stu-id="4cc10-101">Disable-AzContextAutosave</span></span>

## <span data-ttu-id="4cc10-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4cc10-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc10-103">Wyłącz Autozapisywanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc10-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="4cc10-104">Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4cc10-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="4cc10-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4cc10-105">SYNTAX</span></span>

```
Disable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cc10-106">Opis</span><span class="sxs-lookup"><span data-stu-id="4cc10-106">DESCRIPTION</span></span>
<span data-ttu-id="4cc10-107">Wyłącz Autozapisywanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4cc10-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="4cc10-108">Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="4cc10-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="4cc10-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4cc10-109">EXAMPLES</span></span>

### <span data-ttu-id="4cc10-110">Wyłączanie autozapisywania kontekstu</span><span class="sxs-lookup"><span data-stu-id="4cc10-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzContextAutosave
```

<span data-ttu-id="4cc10-111">Wyłącz Autozapis dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4cc10-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="4cc10-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4cc10-112">PARAMETERS</span></span>

### <span data-ttu-id="4cc10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc10-113">-DefaultProfile</span></span>
<span data-ttu-id="4cc10-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="4cc10-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cc10-115">-Zakres</span><span class="sxs-lookup"><span data-stu-id="4cc10-115">-Scope</span></span>
<span data-ttu-id="4cc10-116">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="4cc10-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="4cc10-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cc10-117">-Confirm</span></span>
<span data-ttu-id="4cc10-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cc10-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cc10-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cc10-119">-WhatIf</span></span>
<span data-ttu-id="4cc10-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cc10-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cc10-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4cc10-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cc10-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc10-122">CommonParameters</span></span>
<span data-ttu-id="4cc10-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc10-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc10-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc10-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc10-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cc10-125">INPUTS</span></span>

### <span data-ttu-id="4cc10-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4cc10-126">None</span></span>

## <span data-ttu-id="4cc10-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4cc10-127">OUTPUTS</span></span>

### <span data-ttu-id="4cc10-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="4cc10-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="4cc10-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4cc10-129">NOTES</span></span>

## <span data-ttu-id="4cc10-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cc10-130">RELATED LINKS</span></span>