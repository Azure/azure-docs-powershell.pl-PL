---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmContext.md
ms.openlocfilehash: 99adb0cb38cd5c1e43dbd9f7dd5f81a4bef26beb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717813"
---
# <span data-ttu-id="a452e-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="a452e-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="a452e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a452e-102">SYNOPSIS</span></span>
<span data-ttu-id="a452e-103">Ustawia dzierżawę, abonament i środowisko dla poleceń cmdlet, które mają być używane w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="a452e-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a452e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a452e-104">SYNTAX</span></span>

### <span data-ttu-id="a452e-105">Context (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="a452e-105">Context (Default)</span></span>
```
Set-AzureRmContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a452e-106">Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="a452e-106">TenantObject</span></span>
```
Set-AzureRmContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a452e-107">Abonamentobject</span><span class="sxs-lookup"><span data-stu-id="a452e-107">SubscriptionObject</span></span>
```
Set-AzureRmContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a452e-108">Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a452e-108">Subscription</span></span>
```
Set-AzureRmContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a452e-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="a452e-109">TenantNameOnly</span></span>
```
Set-AzureRmContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a452e-110">Opis</span><span class="sxs-lookup"><span data-stu-id="a452e-110">DESCRIPTION</span></span>
<span data-ttu-id="a452e-111">Polecenie cmdlet Set-AzureRmContext ustawia informacje uwierzytelniające dotyczące apletów poleceń uruchomionych w bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="a452e-111">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="a452e-112">Kontekst obejmuje informacje dotyczące dzierżawy, abonamentu i środowiska.</span><span class="sxs-lookup"><span data-stu-id="a452e-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="a452e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a452e-113">EXAMPLES</span></span>

### <span data-ttu-id="a452e-114">Przykład 1. Ustawianie kontekstu subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a452e-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a452e-115">To polecenie umożliwia ustawienie kontekstu do korzystania z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a452e-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="a452e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a452e-116">PARAMETERS</span></span>

### <span data-ttu-id="a452e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="a452e-117">-Context</span></span>
<span data-ttu-id="a452e-118">Określa kontekst bieżącej sesji.</span><span class="sxs-lookup"><span data-stu-id="a452e-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a452e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a452e-119">-DefaultProfile</span></span>
<span data-ttu-id="a452e-120">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a452e-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a452e-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="a452e-121">-ExtendedProperty</span></span>
<span data-ttu-id="a452e-122">Dodatkowe właściwości kontekstu</span><span class="sxs-lookup"><span data-stu-id="a452e-122">Additional context properties</span></span>

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

### <span data-ttu-id="a452e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a452e-123">-Force</span></span>
<span data-ttu-id="a452e-124">Zastąp istniejący kontekst o tej samej nazwie (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="a452e-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="a452e-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a452e-125">-Name</span></span>
<span data-ttu-id="a452e-126">Nazwa kontekstu</span><span class="sxs-lookup"><span data-stu-id="a452e-126">Name of the context</span></span>

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

### <span data-ttu-id="a452e-127">-Zakres</span><span class="sxs-lookup"><span data-stu-id="a452e-127">-Scope</span></span>
<span data-ttu-id="a452e-128">Określa zakres zmian kontekstu, na przykład wheher zmiany dotyczą tylko procesu cusrrent lub wszystkich sesji uruchomionych przez tego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a452e-128">Determines the scope of context changes, for example, wheher changes apply only to the cusrrent process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a452e-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="a452e-129">-Subscription</span></span>
<span data-ttu-id="a452e-130">Nazwa lub Identyfikator subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a452e-130">Subscription Name or Id</span></span>

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

### <span data-ttu-id="a452e-131">-Subscriptionobject</span><span class="sxs-lookup"><span data-stu-id="a452e-131">-SubscriptionObject</span></span>
<span data-ttu-id="a452e-132">Obiekt subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a452e-132">A subscription object</span></span>

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

### <span data-ttu-id="a452e-133">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="a452e-133">-Tenant</span></span>
<span data-ttu-id="a452e-134">Nazwa lub identyfikator dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a452e-134">Tenant name or ID</span></span>

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

### <span data-ttu-id="a452e-135">-Dzierżawca</span><span class="sxs-lookup"><span data-stu-id="a452e-135">-TenantObject</span></span>
<span data-ttu-id="a452e-136">Obiekt dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a452e-136">A Tenant Object</span></span>

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

### <span data-ttu-id="a452e-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a452e-137">-Confirm</span></span>
<span data-ttu-id="a452e-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a452e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a452e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a452e-139">-WhatIf</span></span>
<span data-ttu-id="a452e-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a452e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a452e-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a452e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a452e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a452e-142">CommonParameters</span></span>
<span data-ttu-id="a452e-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a452e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a452e-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a452e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a452e-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a452e-145">INPUTS</span></span>

### <span data-ttu-id="a452e-146">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a452e-146">PSAzureContext</span></span>
<span data-ttu-id="a452e-147">Parametr "context" przyjmuje wartość typu "PSAzureContext" z potoku</span><span class="sxs-lookup"><span data-stu-id="a452e-147">Parameter 'Context' accepts value of type 'PSAzureContext' from the pipeline</span></span>

## <span data-ttu-id="a452e-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a452e-148">OUTPUTS</span></span>

### <span data-ttu-id="a452e-149">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="a452e-149">PSAzureContext</span></span>

## <span data-ttu-id="a452e-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a452e-150">NOTES</span></span>

## <span data-ttu-id="a452e-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a452e-151">RELATED LINKS</span></span>

[<span data-ttu-id="a452e-152">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="a452e-152">Get-AzureRMContext</span></span>](./Get-AzureRMContext.md)

