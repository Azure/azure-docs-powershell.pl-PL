---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 629e35c5b700477fc46565b2da0e5dcf6f3c5b6f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981345"
---
# <span data-ttu-id="9838a-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="9838a-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="9838a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9838a-102">SYNOPSIS</span></span>
<span data-ttu-id="9838a-103">Wyświetl metadane dotyczące funkcji autozazysowania kontekstu, w tym informacje o tym, czy kontekst jest zapisywany automatycznie, oraz gdzie można znaleźć zapisane informacje kontekstowe i poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="9838a-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="9838a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9838a-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9838a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9838a-105">DESCRIPTION</span></span>
<span data-ttu-id="9838a-106">Wyświetl metadane dotyczące funkcji autozazysowania kontekstu, w tym informacje o tym, czy kontekst jest zapisywany automatycznie, oraz gdzie można znaleźć zapisane informacje kontekstowe i poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="9838a-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="9838a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9838a-107">EXAMPLES</span></span>

### <span data-ttu-id="9838a-108">Uzyskiwanie metadanych zapisywania kontekstowego dla bieżącej sesji</span><span class="sxs-lookup"><span data-stu-id="9838a-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="9838a-109">Uzyskaj szczegółowe informacje na temat tego, czy i gdzie jest zapisywany kontekst.</span><span class="sxs-lookup"><span data-stu-id="9838a-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="9838a-110">W powyższym przykładzie funkcja autozazysowania została wyłączona.</span><span class="sxs-lookup"><span data-stu-id="9838a-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="9838a-111">Uzyskiwanie metadanych zapisywania kontekstowego dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="9838a-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="9838a-112">Szczegółowe informacje o tym, czy i gdzie jest domyślnie zapisywany kontekst dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9838a-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="9838a-113">Pamiętaj, że może to być inne niż ustawienia aktywne w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="9838a-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="9838a-114">W powyższym przykładzie funkcja autozazysowania została włączona i dane są zapisywane w lokalizacji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="9838a-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="9838a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9838a-115">PARAMETERS</span></span>

### <span data-ttu-id="9838a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9838a-116">-DefaultProfile</span></span>
<span data-ttu-id="9838a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="9838a-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9838a-118">— Zakres</span><span class="sxs-lookup"><span data-stu-id="9838a-118">-Scope</span></span>
<span data-ttu-id="9838a-119">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9838a-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="9838a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9838a-120">CommonParameters</span></span>
<span data-ttu-id="9838a-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9838a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9838a-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9838a-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9838a-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9838a-123">INPUTS</span></span>

### <span data-ttu-id="9838a-124">Brak</span><span class="sxs-lookup"><span data-stu-id="9838a-124">None</span></span>

## <span data-ttu-id="9838a-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9838a-125">OUTPUTS</span></span>

### <span data-ttu-id="9838a-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="9838a-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="9838a-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9838a-127">NOTES</span></span>

## <span data-ttu-id="9838a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9838a-128">RELATED LINKS</span></span>
