---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 541306c8216168143e97bff84548e1c8e2a0ee47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704738"
---
# <span data-ttu-id="fd62a-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="fd62a-101">Set-AzContext</span></span>

## <span data-ttu-id="fd62a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fd62a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd62a-103">Ustawia dzierżawę, abonament i środowisko dla poleceń cmdlet, które mają być używane w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="fd62a-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="fd62a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fd62a-104">SYNTAX</span></span>

### <span data-ttu-id="fd62a-105">Context (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fd62a-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd62a-106">Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="fd62a-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd62a-107">Abonamentobject</span><span class="sxs-lookup"><span data-stu-id="fd62a-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd62a-108">Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fd62a-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd62a-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="fd62a-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd62a-110">Opis</span><span class="sxs-lookup"><span data-stu-id="fd62a-110">DESCRIPTION</span></span>
<span data-ttu-id="fd62a-111">Polecenie cmdlet Set-AzContext ustawia informacje uwierzytelniające dotyczące apletów poleceń uruchomionych w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="fd62a-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="fd62a-112">Kontekst obejmuje informacje dotyczące dzierżawy, abonamentu i środowiska.</span><span class="sxs-lookup"><span data-stu-id="fd62a-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="fd62a-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fd62a-113">EXAMPLES</span></span>

### <span data-ttu-id="fd62a-114">Przykład 1. Ustawianie kontekstu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fd62a-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="fd62a-115">To polecenie umożliwia ustawienie kontekstu do korzystania z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="fd62a-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="fd62a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fd62a-116">PARAMETERS</span></span>

### <span data-ttu-id="fd62a-117">-Context</span><span class="sxs-lookup"><span data-stu-id="fd62a-117">-Context</span></span>
<span data-ttu-id="fd62a-118">Określa kontekst bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="fd62a-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd62a-119">-DefaultProfile</span></span>
<span data-ttu-id="fd62a-120">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fd62a-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd62a-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="fd62a-121">-ExtendedProperty</span></span>
<span data-ttu-id="fd62a-122">Dodatkowe właściwości kontekstu</span><span class="sxs-lookup"><span data-stu-id="fd62a-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fd62a-123">-Force</span></span>
<span data-ttu-id="fd62a-124">Zastąp istniejący kontekst o tej samej nazwie (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="fd62a-124">Overwrite the existing context with the same name, if any.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fd62a-125">-Name</span></span>
<span data-ttu-id="fd62a-126">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="fd62a-126">Name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-127">-Zakres</span><span class="sxs-lookup"><span data-stu-id="fd62a-127">-Scope</span></span>
<span data-ttu-id="fd62a-128">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fd62a-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="fd62a-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="fd62a-129">-Subscription</span></span>
<span data-ttu-id="fd62a-130">Nazwa lub Identyfikator subskrypcji, do której należy ustawić kontekst.</span><span class="sxs-lookup"><span data-stu-id="fd62a-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="fd62a-131">Ten parametr ma aliasy-Subscriptionname i-Binding, więc w celu zachowania jasności można go użyć zamiast opcji-Subscription podczas określania nazwy i identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="fd62a-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-132">-Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="fd62a-132">-SubscriptionObject</span></span>
<span data-ttu-id="fd62a-133">Obiekt subskrypcji</span><span class="sxs-lookup"><span data-stu-id="fd62a-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-134">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="fd62a-134">-Tenant</span></span>
<span data-ttu-id="fd62a-135">Nazwa lub identyfikator dzierżawy</span><span class="sxs-lookup"><span data-stu-id="fd62a-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-136">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="fd62a-136">-TenantObject</span></span>
<span data-ttu-id="fd62a-137">Obiekt dzierżawy</span><span class="sxs-lookup"><span data-stu-id="fd62a-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fd62a-138">-Confirm</span></span>
<span data-ttu-id="fd62a-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd62a-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd62a-140">-WhatIf</span></span>
<span data-ttu-id="fd62a-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd62a-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd62a-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fd62a-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd62a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd62a-143">CommonParameters</span></span>
<span data-ttu-id="fd62a-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd62a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd62a-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd62a-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd62a-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fd62a-146">INPUTS</span></span>

### <span data-ttu-id="fd62a-147">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="fd62a-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="fd62a-148">Microsoft. Azure. Commands. profile. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="fd62a-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="fd62a-149">Microsoft. Azure. Commands. profile. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="fd62a-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="fd62a-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fd62a-150">OUTPUTS</span></span>

### <span data-ttu-id="fd62a-151">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="fd62a-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="fd62a-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fd62a-152">NOTES</span></span>

## <span data-ttu-id="fd62a-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fd62a-153">RELATED LINKS</span></span>

[<span data-ttu-id="fd62a-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="fd62a-154">Get-AzContext</span></span>](./Get-AzContext.md)

