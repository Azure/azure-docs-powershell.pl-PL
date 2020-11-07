---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: a55844251e7d84ef24d62195b96b9bd4c3934317
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707234"
---
# <span data-ttu-id="3b210-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="3b210-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="3b210-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b210-102">SYNOPSIS</span></span>
<span data-ttu-id="3b210-103">Odłączenie połączonego konta platformy Azure i usunięcie wszystkich poświadczeń i kontekstów skojarzonych z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="3b210-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="3b210-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b210-104">SYNTAX</span></span>

### <span data-ttu-id="3b210-105">Opis. tekst (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3b210-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b210-106">UserId</span><span class="sxs-lookup"><span data-stu-id="3b210-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b210-107">Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="3b210-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b210-108">AccountName</span><span class="sxs-lookup"><span data-stu-id="3b210-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b210-109">Tekst</span><span class="sxs-lookup"><span data-stu-id="3b210-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b210-110">Opis</span><span class="sxs-lookup"><span data-stu-id="3b210-110">DESCRIPTION</span></span>
<span data-ttu-id="3b210-111">Polecenie cmdlet Disconnect-AzAccount rozłącza połączone konto platformy Azure i usuwa wszystkie poświadczenia i konteksty (informacje o subskrypcji i dzierżawie) skojarzone z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="3b210-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="3b210-112">Po wykonaniu tego polecenia musisz zalogować się ponownie przy użyciu polecenia Connect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="3b210-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="3b210-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b210-113">EXAMPLES</span></span>

### <span data-ttu-id="3b210-114">Wylogowywanie się z bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="3b210-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="3b210-115">Wylogowuje się z konta platformy Azure skojarzonego z bieżącym kontekstem.</span><span class="sxs-lookup"><span data-stu-id="3b210-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="3b210-116">Wylogowanie konta skojarzonego z określonym kontekstem</span><span class="sxs-lookup"><span data-stu-id="3b210-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="3b210-117">Wylogowuje konto skojarzone z danym kontekstem (nazwane "praca").</span><span class="sxs-lookup"><span data-stu-id="3b210-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="3b210-118">Ponieważ w tym polu jest używany zakres "CurrentUser", wszystkie poświadczenia i konteksty zostaną trwale usunięte.</span><span class="sxs-lookup"><span data-stu-id="3b210-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="3b210-119">Wylogowywanie określonego użytkownika</span><span class="sxs-lookup"><span data-stu-id="3b210-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="3b210-120">Wylogowuje user1@contoso.org użytkownika "użytkownik — wszystkie poświadczenia i wszystkie konteksty skojarzone z tym użytkownikiem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="3b210-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="3b210-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b210-121">PARAMETERS</span></span>

### <span data-ttu-id="3b210-122">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="3b210-122">-ApplicationId</span></span>
<span data-ttu-id="3b210-123">Identyfikator podmiotu zabezpieczeń (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="3b210-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="3b210-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="3b210-124">-AzureContext</span></span>
<span data-ttu-id="3b210-125">Świetle</span><span class="sxs-lookup"><span data-stu-id="3b210-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b210-126">-Ontextname</span><span class="sxs-lookup"><span data-stu-id="3b210-126">-ContextName</span></span>
<span data-ttu-id="3b210-127">Nazwa kontekstu do wylogowania</span><span class="sxs-lookup"><span data-stu-id="3b210-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="3b210-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b210-128">-DefaultProfile</span></span>
<span data-ttu-id="3b210-129">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3b210-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b210-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3b210-130">-InputObject</span></span>
<span data-ttu-id="3b210-131">Obiekt konta do usunięcia</span><span class="sxs-lookup"><span data-stu-id="3b210-131">The account object to remove</span></span>

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

### <span data-ttu-id="3b210-132">-Zakres</span><span class="sxs-lookup"><span data-stu-id="3b210-132">-Scope</span></span>
<span data-ttu-id="3b210-133">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3b210-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3b210-134">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="3b210-134">-TenantId</span></span>
<span data-ttu-id="3b210-135">Identyfikator dzierżawy (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="3b210-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="3b210-136">-Username</span><span class="sxs-lookup"><span data-stu-id="3b210-136">-Username</span></span>
<span data-ttu-id="3b210-137">Nazwa użytkownika formularza ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="3b210-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="3b210-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3b210-138">-Confirm</span></span>
<span data-ttu-id="3b210-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b210-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b210-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b210-140">-WhatIf</span></span>
<span data-ttu-id="3b210-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b210-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b210-142">Polecenie cmdlet nie jest wykonywane.</span><span class="sxs-lookup"><span data-stu-id="3b210-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="3b210-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b210-143">CommonParameters</span></span>
<span data-ttu-id="3b210-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b210-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b210-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b210-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b210-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b210-146">INPUTS</span></span>

### <span data-ttu-id="3b210-147">Microsoft. Azure. Commands. profile. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="3b210-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="3b210-148">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="3b210-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="3b210-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b210-149">OUTPUTS</span></span>

### <span data-ttu-id="3b210-150">Microsoft. Azure. Commands. profile. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="3b210-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="3b210-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b210-151">NOTES</span></span>

## <span data-ttu-id="3b210-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b210-152">RELATED LINKS</span></span>