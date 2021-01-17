---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327810"
---
# <span data-ttu-id="3c039-101">Get-AzContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="3c039-101">Get-AzContextAutosaveSetting</span></span>

## <span data-ttu-id="3c039-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c039-102">SYNOPSIS</span></span>
<span data-ttu-id="3c039-103">Wyświetla metadane dotyczące funkcji automatycznego zapisu kontekstowego, w tym informacje o tym, czy kontekst jest automatycznie zapisywany, oraz gdzie można znaleźć zapisane informacje o kontekście i poświadczeniach.</span><span class="sxs-lookup"><span data-stu-id="3c039-103">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="3c039-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c039-104">SYNTAX</span></span>

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c039-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c039-105">DESCRIPTION</span></span>
<span data-ttu-id="3c039-106">Wyświetla metadane dotyczące funkcji automatycznego zapisu kontekstowego, w tym informacje o tym, czy kontekst jest automatycznie zapisywany, oraz gdzie można znaleźć zapisane informacje o kontekście i poświadczeniach.</span><span class="sxs-lookup"><span data-stu-id="3c039-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="3c039-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c039-107">EXAMPLES</span></span>

### <span data-ttu-id="3c039-108">Pobieranie metadanych kontekstu zapisu dla bieżącej sesji</span><span class="sxs-lookup"><span data-stu-id="3c039-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="3c039-109">Uzyskaj szczegółowe informacje o tym, czy i gdzie kontekst jest zapisany.</span><span class="sxs-lookup"><span data-stu-id="3c039-109">Get details about whether and where the context is saved.</span></span>  <span data-ttu-id="3c039-110">W powyższym przykładzie funkcja Autozapis została wyłączona.</span><span class="sxs-lookup"><span data-stu-id="3c039-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="3c039-111">Pobieranie metadanych kontekstu zapisu dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="3c039-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="3c039-112">Uzyskaj szczegółowe informacje o tym, czy i gdzie kontekst jest domyślnie zapisywany dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3c039-112">Get details about whether and where the context is saved by default for the current user.</span></span>  <span data-ttu-id="3c039-113">Zauważ, że może to być inne niż ustawienia aktywne w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="3c039-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="3c039-114">W powyższym przykładzie funkcja Autozapis została włączona, a dane są zapisywane w lokalizacji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="3c039-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="3c039-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c039-115">PARAMETERS</span></span>

### <span data-ttu-id="3c039-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c039-116">-DefaultProfile</span></span>
<span data-ttu-id="3c039-117">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3c039-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3c039-118">-Zakres</span><span class="sxs-lookup"><span data-stu-id="3c039-118">-Scope</span></span>
<span data-ttu-id="3c039-119">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3c039-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3c039-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c039-120">CommonParameters</span></span>
<span data-ttu-id="3c039-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c039-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c039-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c039-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c039-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c039-123">INPUTS</span></span>

### <span data-ttu-id="3c039-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3c039-124">None</span></span>

## <span data-ttu-id="3c039-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c039-125">OUTPUTS</span></span>

### <span data-ttu-id="3c039-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="3c039-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>

## <span data-ttu-id="3c039-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c039-127">NOTES</span></span>

## <span data-ttu-id="3c039-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c039-128">RELATED LINKS</span></span>
