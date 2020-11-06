---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
ms.openlocfilehash: d1b401c1ae806d48b9cb9969c36ef72d104076eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546104"
---
# <span data-ttu-id="5a6ac-101">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="5a6ac-101">Remove-AzureRmAccount</span></span>

## <span data-ttu-id="5a6ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a6ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5a6ac-103">Usuwanie wszystkich poświadczeń i kontekstów skojarzonych z danym kontem.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-103">Remove all credentials and contexts associated with the given account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a6ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a6ac-104">SYNTAX</span></span>

### <span data-ttu-id="5a6ac-105">Opis. tekst (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5a6ac-105">ContextName (Default)</span></span>
```
Remove-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6ac-106">UserId</span><span class="sxs-lookup"><span data-stu-id="5a6ac-106">UserId</span></span>
```
Remove-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6ac-107">Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="5a6ac-107">ServicePrincipal</span></span>
```
Remove-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6ac-108">AccountName</span><span class="sxs-lookup"><span data-stu-id="5a6ac-108">AccountObject</span></span>
```
Remove-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6ac-109">Tekst</span><span class="sxs-lookup"><span data-stu-id="5a6ac-109">ContextObject</span></span>
```
Remove-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a6ac-110">Opis</span><span class="sxs-lookup"><span data-stu-id="5a6ac-110">DESCRIPTION</span></span>
<span data-ttu-id="5a6ac-111">Usuń wszystkie poświadczenia i konteksty (informacje o subskrypcji i dzierżawie) skojarzone z danym kontem.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-111">Remove all credentials, and contexts (subscription and tenant information) associated with the given account.</span></span>  <span data-ttu-id="5a6ac-112">Po wykonaniu tego polecenia musisz zalogować się ponownie przy użyciu Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="5a6ac-112">After executing this cmdlet, you will need to login again using Add-AzureRmAccount</span></span>

## <span data-ttu-id="5a6ac-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a6ac-113">EXAMPLES</span></span>

### <span data-ttu-id="5a6ac-114">Logowanie się do konta curent</span><span class="sxs-lookup"><span data-stu-id="5a6ac-114">Log out the curent account</span></span>
```
PS C:\> Remove-AzureRmAccount
```

<span data-ttu-id="5a6ac-115">Wylogowuje konto skojarzone z bieżącym kontekstem.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-115">Logs out the account associated with the current context.</span></span>

### <span data-ttu-id="5a6ac-116">Wylogowywanie konta skojarzonego z określonym kontekstem</span><span class="sxs-lookup"><span data-stu-id="5a6ac-116">Log out the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Remove-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="5a6ac-117">Wylogowuje konto skojarzone z danym kontekstem (nazwane "praca").</span><span class="sxs-lookup"><span data-stu-id="5a6ac-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="5a6ac-118">Ponieważ w tym polu jest używany zakres "CurrentUser", wszystkie poświadczenia i konteksty zostaną trwale usunięte.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="5a6ac-119">Wylogowywanie określonego użytkownika</span><span class="sxs-lookup"><span data-stu-id="5a6ac-119">Log out a particular user</span></span>
```
PS C:\> Remove-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="5a6ac-120">Wylogowuje user1@contoso.org użytkownika "użytkownik — wszystkie poświadczenia i wszystkie konteksty skojarzone z tym użytkownikiem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="5a6ac-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a6ac-121">PARAMETERS</span></span>

### <span data-ttu-id="5a6ac-122">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="5a6ac-122">-ApplicationId</span></span>
<span data-ttu-id="5a6ac-123">Identyfikator podmiotu zabezpieczeń (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="5a6ac-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ac-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="5a6ac-124">-AzureContext</span></span>
<span data-ttu-id="5a6ac-125">Świetle</span><span class="sxs-lookup"><span data-stu-id="5a6ac-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ac-126">-Ontextname</span><span class="sxs-lookup"><span data-stu-id="5a6ac-126">-ContextName</span></span>
<span data-ttu-id="5a6ac-127">Nazwa kontekstu do wylogowania</span><span class="sxs-lookup"><span data-stu-id="5a6ac-127">Name of the context to log out of</span></span>

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ac-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a6ac-128">-DefaultProfile</span></span>
<span data-ttu-id="5a6ac-129">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5a6ac-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a6ac-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5a6ac-130">-InputObject</span></span>
<span data-ttu-id="5a6ac-131">Obiekt konta do usunięcia</span><span class="sxs-lookup"><span data-stu-id="5a6ac-131">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ac-132">-Zakres</span><span class="sxs-lookup"><span data-stu-id="5a6ac-132">-Scope</span></span>
<span data-ttu-id="5a6ac-133">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="5a6ac-134">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="5a6ac-134">-TenantId</span></span>
<span data-ttu-id="5a6ac-135">Identyfikator dzierżawy (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="5a6ac-135">Tenant id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ac-136">-Username</span><span class="sxs-lookup"><span data-stu-id="5a6ac-136">-Username</span></span>
<span data-ttu-id="5a6ac-137">Nazwa użytkownika formularza ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="5a6ac-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6ac-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5a6ac-138">-Confirm</span></span>
<span data-ttu-id="5a6ac-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a6ac-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a6ac-140">-WhatIf</span></span>
<span data-ttu-id="5a6ac-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a6ac-142">Polecenie cmdlet nie jest wykonywane.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="5a6ac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6ac-143">CommonParameters</span></span>
<span data-ttu-id="5a6ac-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a6ac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6ac-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a6ac-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6ac-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a6ac-146">INPUTS</span></span>

### <span data-ttu-id="5a6ac-147">Microsoft. Azure. Commands. profile. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="5a6ac-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="5a6ac-148">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="5a6ac-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="5a6ac-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a6ac-149">OUTPUTS</span></span>

### <span data-ttu-id="5a6ac-150">Microsoft. Azure. Commands. profile. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="5a6ac-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="5a6ac-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a6ac-151">NOTES</span></span>

## <span data-ttu-id="5a6ac-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a6ac-152">RELATED LINKS</span></span>

