---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 5dcb1636dc4ecc4556bea14f8b3cd52bec7c0927
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890162"
---
# <span data-ttu-id="37115-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="37115-101">Set-AzContext</span></span>

## <span data-ttu-id="37115-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37115-102">SYNOPSIS</span></span>
<span data-ttu-id="37115-103">Ustawia dzierżawę, abonament i środowisko dla poleceń cmdlet, które mają być używane w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="37115-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="37115-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37115-104">SYNTAX</span></span>

### <span data-ttu-id="37115-105">Context (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="37115-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37115-106">Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="37115-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37115-107">Abonamentobject</span><span class="sxs-lookup"><span data-stu-id="37115-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37115-108">Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="37115-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37115-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="37115-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37115-110">Opis</span><span class="sxs-lookup"><span data-stu-id="37115-110">DESCRIPTION</span></span>
<span data-ttu-id="37115-111">Polecenie cmdlet Set-AzContext ustawia informacje uwierzytelniające dotyczące apletów poleceń uruchomionych w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="37115-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="37115-112">Kontekst obejmuje informacje dotyczące dzierżawy, abonamentu i środowiska.</span><span class="sxs-lookup"><span data-stu-id="37115-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="37115-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37115-113">EXAMPLES</span></span>

### <span data-ttu-id="37115-114">Przykład 1. Ustawianie kontekstu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="37115-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="37115-115">To polecenie umożliwia ustawienie kontekstu do korzystania z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="37115-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="37115-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37115-116">PARAMETERS</span></span>

### <span data-ttu-id="37115-117">-Context</span><span class="sxs-lookup"><span data-stu-id="37115-117">-Context</span></span>
<span data-ttu-id="37115-118">Określa kontekst bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="37115-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="37115-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37115-119">-DefaultProfile</span></span>
<span data-ttu-id="37115-120">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37115-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37115-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="37115-121">-ExtendedProperty</span></span>
<span data-ttu-id="37115-122">Dodatkowe właściwości kontekstu</span><span class="sxs-lookup"><span data-stu-id="37115-122">Additional context properties</span></span>

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

### <span data-ttu-id="37115-123">-Force</span><span class="sxs-lookup"><span data-stu-id="37115-123">-Force</span></span>
<span data-ttu-id="37115-124">Zastąp istniejący kontekst o tej samej nazwie (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="37115-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="37115-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37115-125">-Name</span></span>
<span data-ttu-id="37115-126">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="37115-126">Name of the context</span></span>

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

### <span data-ttu-id="37115-127">-Zakres</span><span class="sxs-lookup"><span data-stu-id="37115-127">-Scope</span></span>
<span data-ttu-id="37115-128">Określa zakres zmian kontekstu, na przykład, czy zmiany są stosowane tylko do bieżącego procesu, czy do wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="37115-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="37115-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="37115-129">-Subscription</span></span>
<span data-ttu-id="37115-130">Nazwa lub Identyfikator subskrypcji, do której należy ustawić kontekst.</span><span class="sxs-lookup"><span data-stu-id="37115-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="37115-131">Ten parametr ma aliasy-Subscriptionname i-Binding, więc w celu zachowania jasności można go użyć zamiast opcji-Subscription podczas określania nazwy i identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="37115-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="37115-132">-Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="37115-132">-SubscriptionObject</span></span>
<span data-ttu-id="37115-133">Obiekt subskrypcji</span><span class="sxs-lookup"><span data-stu-id="37115-133">A subscription object</span></span>

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

### <span data-ttu-id="37115-134">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="37115-134">-Tenant</span></span>
<span data-ttu-id="37115-135">Nazwa lub identyfikator dzierżawy</span><span class="sxs-lookup"><span data-stu-id="37115-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="37115-136">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="37115-136">-TenantObject</span></span>
<span data-ttu-id="37115-137">Obiekt dzierżawy</span><span class="sxs-lookup"><span data-stu-id="37115-137">A Tenant Object</span></span>

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

### <span data-ttu-id="37115-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37115-138">-Confirm</span></span>
<span data-ttu-id="37115-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37115-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37115-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37115-140">-WhatIf</span></span>
<span data-ttu-id="37115-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37115-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="37115-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37115-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37115-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37115-143">CommonParameters</span></span>
<span data-ttu-id="37115-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37115-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37115-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37115-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37115-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37115-146">INPUTS</span></span>

### <span data-ttu-id="37115-147">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="37115-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="37115-148">Microsoft. Azure. Commands. profile. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="37115-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="37115-149">Microsoft. Azure. Commands. profile. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="37115-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="37115-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37115-150">OUTPUTS</span></span>

### <span data-ttu-id="37115-151">Microsoft. Azure. Commands. profile. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="37115-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="37115-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37115-152">NOTES</span></span>

## <span data-ttu-id="37115-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37115-153">RELATED LINKS</span></span>

[<span data-ttu-id="37115-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="37115-154">Get-AzContext</span></span>](./Get-AzContext.md)

