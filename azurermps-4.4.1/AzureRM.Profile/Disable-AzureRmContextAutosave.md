---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 85c3791e9947ce6f7ad2ce365239da16cec17b19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553167"
---
# <span data-ttu-id="72242-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="72242-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="72242-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72242-102">SYNOPSIS</span></span>
<span data-ttu-id="72242-103">Wyłącz Autozapisywanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72242-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="72242-104">Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72242-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72242-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72242-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72242-106">Opis</span><span class="sxs-lookup"><span data-stu-id="72242-106">DESCRIPTION</span></span>
<span data-ttu-id="72242-107">Wyłącz Autozapisywanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="72242-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="72242-108">Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="72242-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="72242-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72242-109">EXAMPLES</span></span>

### <span data-ttu-id="72242-110">Wyłączanie autozapisywania kontekstu</span><span class="sxs-lookup"><span data-stu-id="72242-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="72242-111">Wyłącz Autozapis dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="72242-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="72242-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72242-112">PARAMETERS</span></span>

### <span data-ttu-id="72242-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72242-113">-DefaultProfile</span></span>
<span data-ttu-id="72242-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="72242-114">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72242-115">-Zakres</span><span class="sxs-lookup"><span data-stu-id="72242-115">-Scope</span></span>
<span data-ttu-id="72242-116">Określa zakres zmian kontekstu, na przykład wheher zmiany dotyczą tylko procesu cusrrent lub wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="72242-116">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user</span></span>

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

### <span data-ttu-id="72242-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72242-117">-Confirm</span></span>
<span data-ttu-id="72242-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72242-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72242-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72242-119">-WhatIf</span></span>
<span data-ttu-id="72242-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72242-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72242-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72242-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72242-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72242-122">CommonParameters</span></span>
<span data-ttu-id="72242-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72242-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72242-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72242-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72242-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72242-125">INPUTS</span></span>

### <span data-ttu-id="72242-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="72242-126">None</span></span>

## <span data-ttu-id="72242-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72242-127">OUTPUTS</span></span>

### <span data-ttu-id="72242-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="72242-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="72242-129">Informacje na temat bieżących ustawień Autozapisu, w tym to, czy włączono funkcję Autozapisu dla bieżącego użytkownika, a także gdzie są zapisywane pliki kontekstowe i poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="72242-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="72242-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72242-130">NOTES</span></span>

## <span data-ttu-id="72242-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72242-131">RELATED LINKS</span></span>

