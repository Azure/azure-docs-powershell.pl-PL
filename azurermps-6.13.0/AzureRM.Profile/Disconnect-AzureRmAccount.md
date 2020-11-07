---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e5fbecea64a15569fbd6319f3f3be5ff4102153e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719067"
---
# <span data-ttu-id="d4e66-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="d4e66-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="d4e66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4e66-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e66-103">Odłączenie połączonego konta platformy Azure i usunięcie wszystkich poświadczeń i kontekstów skojarzonych z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="d4e66-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4e66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4e66-104">SYNTAX</span></span>

### <span data-ttu-id="d4e66-105">Opis. tekst (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d4e66-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e66-106">UserId</span><span class="sxs-lookup"><span data-stu-id="d4e66-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e66-107">Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="d4e66-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e66-108">AccountName</span><span class="sxs-lookup"><span data-stu-id="d4e66-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4e66-109">Tekst</span><span class="sxs-lookup"><span data-stu-id="d4e66-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e66-110">Opis</span><span class="sxs-lookup"><span data-stu-id="d4e66-110">DESCRIPTION</span></span>
<span data-ttu-id="d4e66-111">Polecenie cmdlet Disconnect-AzureRmAccount rozłącza połączone konto platformy Azure i usuwa wszystkie poświadczenia i konteksty (informacje o subskrypcji i dzierżawie) skojarzone z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="d4e66-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="d4e66-112">Po wykonaniu tego polecenia musisz zalogować się ponownie przy użyciu polecenia Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="d4e66-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="d4e66-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4e66-113">EXAMPLES</span></span>

### <span data-ttu-id="d4e66-114">Wylogowywanie się z bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="d4e66-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="d4e66-115">Wylogowuje się z konta platformy Azure skojarzonego z bieżącym kontekstem.</span><span class="sxs-lookup"><span data-stu-id="d4e66-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="d4e66-116">Wylogowanie konta skojarzonego z określonym kontekstem</span><span class="sxs-lookup"><span data-stu-id="d4e66-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="d4e66-117">Wylogowuje konto skojarzone z danym kontekstem (nazwane "praca").</span><span class="sxs-lookup"><span data-stu-id="d4e66-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="d4e66-118">Ponieważ w tym polu jest używany zakres "CurrentUser", wszystkie poświadczenia i konteksty zostaną trwale usunięte.</span><span class="sxs-lookup"><span data-stu-id="d4e66-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="d4e66-119">Wylogowywanie określonego użytkownika</span><span class="sxs-lookup"><span data-stu-id="d4e66-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="d4e66-120">Wylogowuje user1@contoso.org użytkownika "użytkownik — wszystkie poświadczenia i wszystkie konteksty skojarzone z tym użytkownikiem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="d4e66-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="d4e66-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4e66-121">PARAMETERS</span></span>

### <span data-ttu-id="d4e66-122">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="d4e66-122">-ApplicationId</span></span>
<span data-ttu-id="d4e66-123">Identyfikator podmiotu zabezpieczeń (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="d4e66-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="d4e66-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="d4e66-124">-AzureContext</span></span>
<span data-ttu-id="d4e66-125">Świetle</span><span class="sxs-lookup"><span data-stu-id="d4e66-125">Context</span></span>

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

### <span data-ttu-id="d4e66-126">-Ontextname</span><span class="sxs-lookup"><span data-stu-id="d4e66-126">-ContextName</span></span>
<span data-ttu-id="d4e66-127">Nazwa kontekstu do wylogowania</span><span class="sxs-lookup"><span data-stu-id="d4e66-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="d4e66-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e66-128">-DefaultProfile</span></span>
<span data-ttu-id="d4e66-129">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d4e66-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4e66-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d4e66-130">-InputObject</span></span>
<span data-ttu-id="d4e66-131">Obiekt konta do usunięcia</span><span class="sxs-lookup"><span data-stu-id="d4e66-131">The account object to remove</span></span>

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

### <span data-ttu-id="d4e66-132">-Zakres</span><span class="sxs-lookup"><span data-stu-id="d4e66-132">-Scope</span></span>
<span data-ttu-id="d4e66-133">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d4e66-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="d4e66-134">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="d4e66-134">-TenantId</span></span>
<span data-ttu-id="d4e66-135">Identyfikator dzierżawy (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="d4e66-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="d4e66-136">-Username</span><span class="sxs-lookup"><span data-stu-id="d4e66-136">-Username</span></span>
<span data-ttu-id="d4e66-137">Nazwa użytkownika formularza ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="d4e66-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="d4e66-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d4e66-138">-Confirm</span></span>
<span data-ttu-id="d4e66-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4e66-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e66-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e66-140">-WhatIf</span></span>
<span data-ttu-id="d4e66-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4e66-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e66-142">Polecenie cmdlet nie jest wykonywane.</span><span class="sxs-lookup"><span data-stu-id="d4e66-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="d4e66-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e66-143">CommonParameters</span></span>
<span data-ttu-id="d4e66-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e66-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e66-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e66-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e66-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4e66-146">INPUTS</span></span>

### <span data-ttu-id="d4e66-147">Microsoft. Azure. Commands. profile. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="d4e66-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>
<span data-ttu-id="d4e66-148">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4e66-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d4e66-149">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="d4e66-149">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="d4e66-150">Parametry: AzureContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d4e66-150">Parameters: AzureContext (ByValue)</span></span>

## <span data-ttu-id="d4e66-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4e66-151">OUTPUTS</span></span>

### <span data-ttu-id="d4e66-152">Microsoft. Azure. Commands. profile. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="d4e66-152">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="d4e66-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4e66-153">NOTES</span></span>

## <span data-ttu-id="d4e66-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4e66-154">RELATED LINKS</span></span>
