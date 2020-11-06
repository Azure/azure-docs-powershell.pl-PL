---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmContextAutosave.md
ms.openlocfilehash: 622cbd399f554173bbe9734429f4ae787fe94d0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525034"
---
# <span data-ttu-id="fc758-101">Disable-AzureRmContextAutosave</span><span class="sxs-lookup"><span data-stu-id="fc758-101">Disable-AzureRmContextAutosave</span></span>

## <span data-ttu-id="fc758-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc758-102">SYNOPSIS</span></span>
<span data-ttu-id="fc758-103">Wyłącz Autozapisywanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fc758-103">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="fc758-104">Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc758-104">Your login information will be forgotten the next time you open a PowerShell window</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc758-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc758-105">SYNTAX</span></span>

```
Disable-AzureRmContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc758-106">Opis</span><span class="sxs-lookup"><span data-stu-id="fc758-106">DESCRIPTION</span></span>
<span data-ttu-id="fc758-107">Wyłącz Autozapisywanie poświadczeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="fc758-107">Turn off autosaving Azure credentials.</span></span>  <span data-ttu-id="fc758-108">Informacje logowania zostaną zapomniane podczas następnego otwarcia okna programu PowerShell.</span><span class="sxs-lookup"><span data-stu-id="fc758-108">Your login information will be forgotten the next time you open a PowerShell window</span></span>

## <span data-ttu-id="fc758-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc758-109">EXAMPLES</span></span>

### <span data-ttu-id="fc758-110">Wyłączanie autozapisywania kontekstu</span><span class="sxs-lookup"><span data-stu-id="fc758-110">Disable autosaving the context</span></span>
```
PS C:\> Disable-AzureRmContextAutosave
```

<span data-ttu-id="fc758-111">Wyłącz Autozapis dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fc758-111">Disable autosave for the current user.</span></span>

## <span data-ttu-id="fc758-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc758-112">PARAMETERS</span></span>

### <span data-ttu-id="fc758-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc758-113">-DefaultProfile</span></span>
<span data-ttu-id="fc758-114">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fc758-114">The credentials, tenant and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc758-115">-Zakres</span><span class="sxs-lookup"><span data-stu-id="fc758-115">-Scope</span></span>
<span data-ttu-id="fc758-116">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fc758-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc758-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc758-117">-Confirm</span></span>
<span data-ttu-id="fc758-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc758-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc758-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc758-119">-WhatIf</span></span>
<span data-ttu-id="fc758-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc758-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc758-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc758-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc758-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc758-122">CommonParameters</span></span>
<span data-ttu-id="fc758-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc758-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc758-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc758-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc758-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc758-125">INPUTS</span></span>

### <span data-ttu-id="fc758-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fc758-126">None</span></span>

## <span data-ttu-id="fc758-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc758-127">OUTPUTS</span></span>

### <span data-ttu-id="fc758-128">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="fc758-128">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="fc758-129">Informacje na temat bieżących ustawień Autozapisu, w tym to, czy włączono funkcję Autozapisu dla bieżącego użytkownika, a także gdzie są zapisywane pliki kontekstowe i poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fc758-129">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="fc758-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc758-130">NOTES</span></span>

## <span data-ttu-id="fc758-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc758-131">RELATED LINKS</span></span>

