---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmContextAutosaveSetting.md
ms.openlocfilehash: d0d6c69bb85fcdf851f0f134bb376252525aec91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549635"
---
# <span data-ttu-id="43191-101">Get-AzureRmContextAutosaveSetting</span><span class="sxs-lookup"><span data-stu-id="43191-101">Get-AzureRmContextAutosaveSetting</span></span>

## <span data-ttu-id="43191-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43191-102">SYNOPSIS</span></span>
<span data-ttu-id="43191-103">Wyświetlanie metadanych funkcji automatycznego zapisu kontekstowego, w tym whterh, że kontekst jest automatycznie aved i gdzie można znaleźć zapisane informacje o kontekście i poświadczeniach.</span><span class="sxs-lookup"><span data-stu-id="43191-103">Display metadata about the context autosave feature, including whterh the context is automaticallys aved, and where saved context and credential information cna be found.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43191-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43191-104">SYNTAX</span></span>

```
Get-AzureRmContextAutosaveSetting [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43191-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43191-105">DESCRIPTION</span></span>
<span data-ttu-id="43191-106">Wyświetla metadane dotyczące funkcji automatycznego zapisu kontekstowego, w tym informacje o tym, czy kontekst jest automatycznie zapisywany, oraz gdzie można znaleźć zapisane informacje o kontekście i poświadczeniach.</span><span class="sxs-lookup"><span data-stu-id="43191-106">Display metadata about the context autosave feature, including whether the context is automatically saved, and where saved context and credential information can be found.</span></span>

## <span data-ttu-id="43191-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43191-107">EXAMPLES</span></span>

### <span data-ttu-id="43191-108">Pobieranie metadanych kontekstu zapisu dla bieżącej sesji</span><span class="sxs-lookup"><span data-stu-id="43191-108">Get context save metadata for the current session</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

<span data-ttu-id="43191-109">Uzyskaj szczegółowe informacje o tym, czy WEHERE jest zapisany w kontekście.</span><span class="sxs-lookup"><span data-stu-id="43191-109">Get details about whether and wehere the context is saved.</span></span>  <span data-ttu-id="43191-110">W powyższym przykładzie funkcja Autozapis została wyłączona.</span><span class="sxs-lookup"><span data-stu-id="43191-110">In the above example, the autosave feature has been disabled.</span></span>

### <span data-ttu-id="43191-111">Pobieranie metadanych kontekstu zapisu dla bieżącego użytkownika</span><span class="sxs-lookup"><span data-stu-id="43191-111">Get context save metadata for the current user</span></span>
```
PS C:\> Get-AzureRmContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

<span data-ttu-id="43191-112">Uzyskaj szczegółowe informacje o tym, czy WEHERE kontekstu jest domyślnie zapisywany dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="43191-112">Get details about whether and wehere the context is saved by default for the current user.</span></span>  <span data-ttu-id="43191-113">Zauważ, że może to być inne niż ustawienia aktywne w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="43191-113">Note that this may be different than the settings that are active in the current session.</span></span> <span data-ttu-id="43191-114">W powyższym przykładzie funkcja Autozapis została włączona, a dane są zapisywane w lokalizacji domyślnej.</span><span class="sxs-lookup"><span data-stu-id="43191-114">In the above example, the autosave feature has been enabled, and data is saved to the default location.</span></span>

## <span data-ttu-id="43191-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43191-115">PARAMETERS</span></span>

### <span data-ttu-id="43191-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43191-116">-DefaultProfile</span></span>
<span data-ttu-id="43191-117">Poświadczenia, konto, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="43191-117">The credentials, account, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43191-118">-Zakres</span><span class="sxs-lookup"><span data-stu-id="43191-118">-Scope</span></span>
<span data-ttu-id="43191-119">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="43191-119">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="43191-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43191-120">CommonParameters</span></span>
<span data-ttu-id="43191-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43191-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43191-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43191-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43191-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43191-123">INPUTS</span></span>

### <span data-ttu-id="43191-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="43191-124">None</span></span>

## <span data-ttu-id="43191-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43191-125">OUTPUTS</span></span>

### <span data-ttu-id="43191-126">Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings</span><span class="sxs-lookup"><span data-stu-id="43191-126">Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings</span></span>
<span data-ttu-id="43191-127">Informacje na temat bieżących ustawień Autozapisu, w tym to, czy włączono funkcję Autozapisu dla bieżącego użytkownika, a także gdzie są zapisywane pliki kontekstowe i poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="43191-127">Information about the current Autosave settings, including whether Autosave is enabled for the current user, and where context and credential files are saved.</span></span>

## <span data-ttu-id="43191-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43191-128">NOTES</span></span>

## <span data-ttu-id="43191-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43191-129">RELATED LINKS</span></span>

