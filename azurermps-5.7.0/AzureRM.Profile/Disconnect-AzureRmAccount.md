---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e72e326fd3251a9b3150b9def06e2fb60afb7d82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718488"
---
# <span data-ttu-id="627fb-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="627fb-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="627fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="627fb-102">SYNOPSIS</span></span>
<span data-ttu-id="627fb-103">Odłączenie połączonego konta platformy Azure i usunięcie wszystkich poświadczeń i kontekstów skojarzonych z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="627fb-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="627fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="627fb-104">SYNTAX</span></span>

### <span data-ttu-id="627fb-105">Opis. tekst (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="627fb-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627fb-106">UserId</span><span class="sxs-lookup"><span data-stu-id="627fb-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627fb-107">Serviceprincipal</span><span class="sxs-lookup"><span data-stu-id="627fb-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627fb-108">AccountName</span><span class="sxs-lookup"><span data-stu-id="627fb-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627fb-109">Tekst</span><span class="sxs-lookup"><span data-stu-id="627fb-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="627fb-110">Opis</span><span class="sxs-lookup"><span data-stu-id="627fb-110">DESCRIPTION</span></span>
<span data-ttu-id="627fb-111">Polecenie cmdlet Disconnect-AzureRmAccount rozłącza połączone konto platformy Azure i usuwa wszystkie poświadczenia i konteksty (informacje o subskrypcji i dzierżawie) skojarzone z tym kontem.</span><span class="sxs-lookup"><span data-stu-id="627fb-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>

<span data-ttu-id="627fb-112">Po wykonaniu tego polecenia musisz zalogować się ponownie przy użyciu polecenia Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="627fb-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="627fb-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="627fb-113">EXAMPLES</span></span>

### <span data-ttu-id="627fb-114">Wylogowywanie się z bieżącego konta</span><span class="sxs-lookup"><span data-stu-id="627fb-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="627fb-115">Wylogowuje się z konta platformy Azure skojarzonego z bieżącym kontekstem.</span><span class="sxs-lookup"><span data-stu-id="627fb-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="627fb-116">Wylogowanie konta skojarzonego z określonym kontekstem</span><span class="sxs-lookup"><span data-stu-id="627fb-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="627fb-117">Wylogowuje konto skojarzone z danym kontekstem (nazwane "praca").</span><span class="sxs-lookup"><span data-stu-id="627fb-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="627fb-118">Ponieważ w tym polu jest używany zakres "CurrentUser", wszystkie poświadczenia i konteksty zostaną trwale usunięte.</span><span class="sxs-lookup"><span data-stu-id="627fb-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="627fb-119">Wylogowywanie określonego użytkownika</span><span class="sxs-lookup"><span data-stu-id="627fb-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="627fb-120">Wylogowuje user1@contoso.org użytkownika "użytkownik — wszystkie poświadczenia i wszystkie konteksty skojarzone z tym użytkownikiem zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="627fb-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="627fb-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="627fb-121">PARAMETERS</span></span>

### <span data-ttu-id="627fb-122">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="627fb-122">-ApplicationId</span></span>
<span data-ttu-id="627fb-123">Identyfikator podmiotu zabezpieczeń (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="627fb-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627fb-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="627fb-124">-AzureContext</span></span>
<span data-ttu-id="627fb-125">Świetle</span><span class="sxs-lookup"><span data-stu-id="627fb-125">Context</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: ContextObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="627fb-126">-Ontextname</span><span class="sxs-lookup"><span data-stu-id="627fb-126">-ContextName</span></span>
<span data-ttu-id="627fb-127">Nazwa kontekstu do wylogowania</span><span class="sxs-lookup"><span data-stu-id="627fb-127">Name of the context to log out of</span></span>

```yaml
Type: String
Parameter Sets: ContextName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627fb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627fb-128">-DefaultProfile</span></span>
<span data-ttu-id="627fb-129">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="627fb-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="627fb-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="627fb-130">-InputObject</span></span>
<span data-ttu-id="627fb-131">Obiekt konta do usunięcia</span><span class="sxs-lookup"><span data-stu-id="627fb-131">The account object to remove</span></span>

```yaml
Type: PSAzureRmAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="627fb-132">-Zakres</span><span class="sxs-lookup"><span data-stu-id="627fb-132">-Scope</span></span>
<span data-ttu-id="627fb-133">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="627fb-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="627fb-134">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="627fb-134">-TenantId</span></span>
<span data-ttu-id="627fb-135">Identyfikator dzierżawy (unikatowy identyfikator globalny)</span><span class="sxs-lookup"><span data-stu-id="627fb-135">Tenant id (globally unique id)</span></span>

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627fb-136">-Username</span><span class="sxs-lookup"><span data-stu-id="627fb-136">-Username</span></span>
<span data-ttu-id="627fb-137">Nazwa użytkownika formularza ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="627fb-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627fb-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="627fb-138">-Confirm</span></span>
<span data-ttu-id="627fb-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="627fb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="627fb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="627fb-140">-WhatIf</span></span>
<span data-ttu-id="627fb-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="627fb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="627fb-142">Polecenie cmdlet nie jest wykonywane.</span><span class="sxs-lookup"><span data-stu-id="627fb-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="627fb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627fb-143">CommonParameters</span></span>
<span data-ttu-id="627fb-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="627fb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627fb-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="627fb-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627fb-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="627fb-146">INPUTS</span></span>

### <span data-ttu-id="627fb-147">Microsoft. Azure. Commands. profile. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="627fb-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="627fb-148">Microsoft. Azure. Commands. profile. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="627fb-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="627fb-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="627fb-149">OUTPUTS</span></span>

### <span data-ttu-id="627fb-150">Microsoft. Azure. Commands. profile. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="627fb-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="627fb-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="627fb-151">NOTES</span></span>

## <span data-ttu-id="627fb-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="627fb-152">RELATED LINKS</span></span>
