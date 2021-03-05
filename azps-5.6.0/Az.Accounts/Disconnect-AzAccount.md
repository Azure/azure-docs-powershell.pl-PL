---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 4f9dc4bebfa0c7e84c1d52e81796e5c4938e465f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999062"
---
# <span data-ttu-id="f6fc3-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="f6fc3-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="f6fc3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6fc3-102">SYNOPSIS</span></span>
<span data-ttu-id="f6fc3-103">Odłącza połączone konto platformy Azure i usuwa wszystkie poświadczenia i konteksty skojarzone z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="f6fc3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f6fc3-104">SYNTAX</span></span>

### <span data-ttu-id="f6fc3-105">Nazwa kontekstowa (domyślna)</span><span class="sxs-lookup"><span data-stu-id="f6fc3-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6fc3-106">UserId</span><span class="sxs-lookup"><span data-stu-id="f6fc3-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6fc3-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f6fc3-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6fc3-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f6fc3-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6fc3-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="f6fc3-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6fc3-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="f6fc3-110">DESCRIPTION</span></span>
<span data-ttu-id="f6fc3-111">Polecenie Disconnect-AzAccount odłącza połączone konto platformy Azure i usuwa wszystkie poświadczenia i konteksty (informacje o subskrypcji i dzierżawie) skojarzone z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="f6fc3-112">Po wykonaniu tego polecenia cmdlet konieczne będzie zalogowanie się przy użyciu connect-azAccount.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="f6fc3-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f6fc3-113">EXAMPLES</span></span>

### <span data-ttu-id="f6fc3-114">Przykład 1. Wylogowanie bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="f6fc3-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="f6fc3-115">Wyloguje się z konta platformy Azure skojarzonego z bieżącym kontekstem.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="f6fc3-116">Przykład 2. Wylogowanie konta skojarzonego z określonym kontekstem</span><span class="sxs-lookup"><span data-stu-id="f6fc3-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="f6fc3-117">Wyloguje konto skojarzone z danym kontekstem (o nazwie "Praca").</span><span class="sxs-lookup"><span data-stu-id="f6fc3-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="f6fc3-118">Ponieważ korzysta on z zakresu bieżącego użytkownika, wszystkie poświadczenia i konteksty zostaną trwale usunięte.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="f6fc3-119">Przykład 3. Wylogowanie określonego użytkownika</span><span class="sxs-lookup"><span data-stu-id="f6fc3-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="f6fc3-120">Wyloguje ' ' użytkownika — wszystkie poświadczenia i wszystkie konteksty skojarzone z tym użytkownikiem user1@contoso.org zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="f6fc3-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6fc3-121">PARAMETERS</span></span>

### <span data-ttu-id="f6fc3-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f6fc3-122">-ApplicationId</span></span>
<span data-ttu-id="f6fc3-123">Identyfikator ServicePrincipal (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="f6fc3-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="f6fc3-124">— AzureContext</span><span class="sxs-lookup"><span data-stu-id="f6fc3-124">-AzureContext</span></span>
<span data-ttu-id="f6fc3-125">Kontekst</span><span class="sxs-lookup"><span data-stu-id="f6fc3-125">Context</span></span>

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

### <span data-ttu-id="f6fc3-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="f6fc3-126">-ContextName</span></span>
<span data-ttu-id="f6fc3-127">Nazwa kontekstu do wylogowania</span><span class="sxs-lookup"><span data-stu-id="f6fc3-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="f6fc3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6fc3-128">-DefaultProfile</span></span>
<span data-ttu-id="f6fc3-129">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f6fc3-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6fc3-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6fc3-130">-InputObject</span></span>
<span data-ttu-id="f6fc3-131">Obiekt konta do usunięcia</span><span class="sxs-lookup"><span data-stu-id="f6fc3-131">The account object to remove</span></span>

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

### <span data-ttu-id="f6fc3-132">— Zakres</span><span class="sxs-lookup"><span data-stu-id="f6fc3-132">-Scope</span></span>
<span data-ttu-id="f6fc3-133">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="f6fc3-134">- TenantId</span><span class="sxs-lookup"><span data-stu-id="f6fc3-134">-TenantId</span></span>
<span data-ttu-id="f6fc3-135">Identyfikator dzierżawy (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="f6fc3-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="f6fc3-136">- Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="f6fc3-136">-Username</span></span>
<span data-ttu-id="f6fc3-137">Nazwa użytkownika formularza ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="f6fc3-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="f6fc3-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6fc3-138">-Confirm</span></span>
<span data-ttu-id="f6fc3-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6fc3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6fc3-140">-WhatIf</span></span>
<span data-ttu-id="f6fc3-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6fc3-142">Polecenie cmdlet nie jest wykonywane.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="f6fc3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6fc3-143">CommonParameters</span></span>
<span data-ttu-id="f6fc3-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6fc3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6fc3-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6fc3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6fc3-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6fc3-146">INPUTS</span></span>

### <span data-ttu-id="f6fc3-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="f6fc3-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="f6fc3-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="f6fc3-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="f6fc3-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6fc3-149">OUTPUTS</span></span>

### <span data-ttu-id="f6fc3-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="f6fc3-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="f6fc3-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f6fc3-151">NOTES</span></span>

## <span data-ttu-id="f6fc3-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6fc3-152">RELATED LINKS</span></span>
