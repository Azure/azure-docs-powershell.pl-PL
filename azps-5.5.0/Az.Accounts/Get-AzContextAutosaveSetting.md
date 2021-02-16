---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199931"
---
# <span data-ttu-id="8f5d8-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="8f5d8-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="8f5d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f5d8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5d8-103">Wyświetl metadane dotyczące funkcji autozazysowania kontekstu, w tym informacje o tym, czy kontekst jest zapisywany automatycznie, oraz gdzie można znaleźć zapisane informacje kontekstowe i poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="8f5d8-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="8f5d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8f5d8-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8f5d8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8f5d8-105">DESCRIPTION</span></span>
<span data-ttu-id="8f5d8-106">Wyświetl metadane dotyczące funkcji autozazysowania kontekstu, w tym informacje o tym, czy kontekst jest zapisywany automatycznie, oraz gdzie można znaleźć zapisane informacje kontekstowe i poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="8f5d8-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="8f5d8-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8f5d8-107">EXAMPLES</span></span>

### <span data-ttu-id="8f5d8-108">Uzyskiwanie metadanych zapisywania kontekstowego dla bieżącej sesji</span><span class="sxs-lookup"><span data-stu-id="8f5d8-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="8f5d8-109">Uzyskaj szczegółowe informacje na temat tego, czy i gdzie jest zapisywany kontekst.</span><span class="sxs-lookup"><span data-stu-id="8f5d8-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="8f5d8-110">W powyższym przykładzie funkcja autozazysowania została wyłączona.</span><span class="sxs-lookup"><span data-stu-id="8f5d8-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="8f5d8-111">Uzyskiwanie metadanych zapisywania kontekstowego dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="8f5d8-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="8f5d8-112">Szczegółowe informacje o tym, czy i gdzie jest domyślnie zapisywany kontekst dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8f5d8-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="8f5d8-113">Pamiętaj, że może to być inne niż ustawienia aktywne w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="8f5d8-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="8f5d8-114">W powyższym przykładzie włączono funkcję autozazysowania i dane są zapisywane w lokalizacji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="8f5d8-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="8f5d8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f5d8-115">PARAMETERS</span></span>

### <span data-ttu-id="8f5d8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5d8-116">-DefaultProfile</span></span>
<span data-ttu-id="8f5d8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="8f5d8-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f5d8-118">— Zakres</span><span class="sxs-lookup"><span data-stu-id="8f5d8-118">-Scope</span></span>
<span data-ttu-id="8f5d8-119">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="8f5d8-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="8f5d8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5d8-120">CommonParameters</span></span>
<span data-ttu-id="8f5d8-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f5d8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5d8-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f5d8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5d8-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f5d8-123">INPUTS</span></span>

### <span data-ttu-id="8f5d8-124">Brak</span><span class="sxs-lookup"><span data-stu-id="8f5d8-124">None</span></span>

## <span data-ttu-id="8f5d8-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f5d8-125">OUTPUTS</span></span>

### <span data-ttu-id="8f5d8-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="8f5d8-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="8f5d8-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8f5d8-127">NOTES</span></span>

## <span data-ttu-id="8f5d8-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f5d8-128">RELATED LINKS</span></span>
