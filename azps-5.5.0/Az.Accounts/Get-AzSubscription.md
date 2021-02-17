---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: aecdd4a0b5f0ef4465f08441841fb923a273afdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190482"
---
# <span data-ttu-id="3f2b9-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="3f2b9-101">Get-AzSubscription</span></span>

## <span data-ttu-id="3f2b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f2b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3f2b9-103">Uzyskaj subskrypcje dostępne dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="3f2b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3f2b9-104">SYNTAX</span></span>

### <span data-ttu-id="3f2b9-105">ListByIdInTenant (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3f2b9-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f2b9-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="3f2b9-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f2b9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="3f2b9-107">DESCRIPTION</span></span>
<span data-ttu-id="3f2b9-108">Polecenie Get-AzSubscription pobiera identyfikator subskrypcji, nazwę subskrypcji i dzierżawę domową subskrypcji, do których może uzyskać dostęp bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="3f2b9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3f2b9-109">EXAMPLES</span></span>

### <span data-ttu-id="3f2b9-110">Przykład 1. Uzyskiwanie wszystkich subskrypcji we wszystkich dzierżawach</span><span class="sxs-lookup"><span data-stu-id="3f2b9-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="3f2b9-111">To polecenie pobiera wszystkie subskrypcje we wszystkich dzierżawach, które są autoryzowane dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="3f2b9-112">Przykład 2. Uzyskiwanie wszystkich subskrypcji dla określonej dzierżawy</span><span class="sxs-lookup"><span data-stu-id="3f2b9-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="3f2b9-113">Lista wszystkich subskrypcji w danej dzierżawie, które są autoryzowane dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="3f2b9-114">Przykład 3. Uzyskiwanie wszystkich subskrypcji w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="3f2b9-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="3f2b9-115">To polecenie pobiera wszystkie subskrypcje w bieżącej dzierżawie, które są autoryzowane dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="3f2b9-116">Przykład 4. Zmienianie bieżącego kontekstu w celu używania określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3f2b9-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="3f2b9-117">To polecenie pobiera określoną subskrypcję, a następnie ustawia bieżący kontekst do używania.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="3f2b9-118">Wszystkie kolejne polecenia cmdlet w tej sesji używają domyślnie nowej subskrypcji (subskrypcji Contoso 1).</span><span class="sxs-lookup"><span data-stu-id="3f2b9-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="3f2b9-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f2b9-119">PARAMETERS</span></span>

### <span data-ttu-id="3f2b9-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="3f2b9-120">-AsJob</span></span>
<span data-ttu-id="3f2b9-121">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3f2b9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f2b9-122">-DefaultProfile</span></span>
<span data-ttu-id="3f2b9-123">Poświadczenia, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="3f2b9-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f2b9-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f2b9-124">-SubscriptionId</span></span>
<span data-ttu-id="3f2b9-125">Określa identyfikator subskrypcji do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-125">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByIdInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2b9-126">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f2b9-126">-SubscriptionName</span></span>
<span data-ttu-id="3f2b9-127">Określa nazwę subskrypcji do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-127">Specifies the name of the subscription to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByNameInTenant
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2b9-128">- TenantId</span><span class="sxs-lookup"><span data-stu-id="3f2b9-128">-TenantId</span></span>
<span data-ttu-id="3f2b9-129">Określa identyfikator dzierżawy zawierającej subskrypcje do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f2b9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f2b9-130">CommonParameters</span></span>
<span data-ttu-id="3f2b9-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f2b9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f2b9-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f2b9-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f2b9-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3f2b9-133">INPUTS</span></span>

### <span data-ttu-id="3f2b9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="3f2b9-134">System.String</span></span>

## <span data-ttu-id="3f2b9-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f2b9-135">OUTPUTS</span></span>

### <span data-ttu-id="3f2b9-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="3f2b9-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="3f2b9-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3f2b9-137">NOTES</span></span>

## <span data-ttu-id="3f2b9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3f2b9-138">RELATED LINKS</span></span>
