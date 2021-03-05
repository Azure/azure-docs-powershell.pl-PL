---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 03bceaee69bfa739268fa4cb1be8c9699f26f405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010106"
---
# <span data-ttu-id="201b9-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="201b9-101">Set-AzContext</span></span>

## <span data-ttu-id="201b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="201b9-102">SYNOPSIS</span></span>
<span data-ttu-id="201b9-103">Ustawia dzierżawę, subskrypcję i środowisko, z których będą korzystać polecenia cmdlet w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="201b9-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="201b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="201b9-104">SYNTAX</span></span>

### <span data-ttu-id="201b9-105">Kontekst (domyślne)</span><span class="sxs-lookup"><span data-stu-id="201b9-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="201b9-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="201b9-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="201b9-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="201b9-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="201b9-108">Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="201b9-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="201b9-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="201b9-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="201b9-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="201b9-110">DESCRIPTION</span></span>
<span data-ttu-id="201b9-111">Polecenie Set-AzContext ustawia informacje o uwierzytelnianiu dla polecenia cmdlet uruchomionego w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="201b9-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="201b9-112">Kontekst obejmuje informacje o dzierżawie, subskrypcji i środowisku.</span><span class="sxs-lookup"><span data-stu-id="201b9-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="201b9-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="201b9-113">EXAMPLES</span></span>

### <span data-ttu-id="201b9-114">Przykład 1. Ustawianie kontekstu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="201b9-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -Subscription "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="201b9-115">To polecenie ustawia kontekst do korzystania z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="201b9-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="201b9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="201b9-116">PARAMETERS</span></span>

### <span data-ttu-id="201b9-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="201b9-117">-Context</span></span>
<span data-ttu-id="201b9-118">Określa kontekst bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="201b9-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="201b9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201b9-119">-DefaultProfile</span></span>
<span data-ttu-id="201b9-120">Poświadczenia, dzierżawy i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="201b9-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="201b9-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="201b9-121">-ExtendedProperty</span></span>
<span data-ttu-id="201b9-122">Dodatkowe właściwości kontekstowe</span><span class="sxs-lookup"><span data-stu-id="201b9-122">Additional context properties</span></span>

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

### <span data-ttu-id="201b9-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="201b9-123">-Force</span></span>
<span data-ttu-id="201b9-124">Zastąp istniejący kontekst o tej samej nazwie (jeśli taki sam).</span><span class="sxs-lookup"><span data-stu-id="201b9-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="201b9-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="201b9-125">-Name</span></span>
<span data-ttu-id="201b9-126">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="201b9-126">Name of the context</span></span>

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

### <span data-ttu-id="201b9-127">— Zakres</span><span class="sxs-lookup"><span data-stu-id="201b9-127">-Scope</span></span>
<span data-ttu-id="201b9-128">Określa zakres zmian kontekstu, na przykład tego, czy zmiany mają zastosowanie tylko do bieżącego procesu, czy do wszystkich sesji rozpoczętych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="201b9-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="201b9-129">— Subskrypcja</span><span class="sxs-lookup"><span data-stu-id="201b9-129">-Subscription</span></span>
<span data-ttu-id="201b9-130">Nazwa lub identyfikator subskrypcji, dla których należy ustawić kontekst.</span><span class="sxs-lookup"><span data-stu-id="201b9-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="201b9-131">Ten parametr ma aliasy to -SubscriptionName i -SubscriptionId, więc w celu zachowania przejrzystości można użyć każdego z nich zamiast nazwy i identyfikatora zamiast nazwy —Subscription.</span><span class="sxs-lookup"><span data-stu-id="201b9-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="201b9-132">- SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="201b9-132">-SubscriptionObject</span></span>
<span data-ttu-id="201b9-133">Obiekt subskrypcji</span><span class="sxs-lookup"><span data-stu-id="201b9-133">A subscription object</span></span>

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

### <span data-ttu-id="201b9-134">— Dzierżawa</span><span class="sxs-lookup"><span data-stu-id="201b9-134">-Tenant</span></span>
<span data-ttu-id="201b9-135">Nazwa dzierżawy lub identyfikator</span><span class="sxs-lookup"><span data-stu-id="201b9-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="201b9-136">- TenantObject</span><span class="sxs-lookup"><span data-stu-id="201b9-136">-TenantObject</span></span>
<span data-ttu-id="201b9-137">Obiekt Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="201b9-137">A Tenant Object</span></span>

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

### <span data-ttu-id="201b9-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="201b9-138">-Confirm</span></span>
<span data-ttu-id="201b9-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="201b9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="201b9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="201b9-140">-WhatIf</span></span>
<span data-ttu-id="201b9-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="201b9-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="201b9-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="201b9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="201b9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201b9-143">CommonParameters</span></span>
<span data-ttu-id="201b9-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201b9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201b9-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="201b9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201b9-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="201b9-146">INPUTS</span></span>

### <span data-ttu-id="201b9-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="201b9-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="201b9-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="201b9-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="201b9-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="201b9-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="201b9-150">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="201b9-150">OUTPUTS</span></span>

### <span data-ttu-id="201b9-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="201b9-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="201b9-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="201b9-152">NOTES</span></span>

## <span data-ttu-id="201b9-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="201b9-153">RELATED LINKS</span></span>

[<span data-ttu-id="201b9-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="201b9-154">Get-AzContext</span></span>](./Get-AzContext.md)

