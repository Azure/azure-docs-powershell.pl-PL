---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzSubscription.md
ms.openlocfilehash: 24896d405a4760b0db004dcb67f876263c9eb17f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704760"
---
# <span data-ttu-id="d4584-101">Get-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="d4584-101">Get-AzSubscription</span></span>

## <span data-ttu-id="d4584-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4584-102">SYNOPSIS</span></span>
<span data-ttu-id="d4584-103">Uzyskaj subskrypcje, do których bieżące konto może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="d4584-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="d4584-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4584-104">SYNTAX</span></span>

### <span data-ttu-id="d4584-105">ListByIdInTenant (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d4584-105">ListByIdInTenant (Default)</span></span>
```
Get-AzSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4584-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="d4584-106">ListByNameInTenant</span></span>
```
Get-AzSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4584-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d4584-107">DESCRIPTION</span></span>
<span data-ttu-id="d4584-108">Polecenie cmdlet Get-AzSubscription Pobiera identyfikator subskrypcji, nazwę subskrypcji i dzierżawę domową dla subskrypcji, do których może uzyskać dostęp bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="d4584-108">The Get-AzSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="d4584-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4584-109">EXAMPLES</span></span>

### <span data-ttu-id="d4584-110">Przykład 1. Uzyskaj wszystkie subskrypcje we wszystkich dzierżawach</span><span class="sxs-lookup"><span data-stu-id="d4584-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="d4584-111">To polecenie pobiera wszystkie subskrypcje wszystkich dzierżawców autoryzowanych jako bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="d4584-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="d4584-112">Przykład 2: uzyskiwanie wszystkich subskrypcji dla konkretnego dzierżawy</span><span class="sxs-lookup"><span data-stu-id="d4584-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzSubscription -TenantId "aaaa-aaaa-aaaa-aaaa"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="d4584-113">Wyświetlanie wszystkich subskrypcji w danej dzierżawie autoryzowanych dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="d4584-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="d4584-114">Przykład 3: uzyskiwanie wszystkich subskrypcji w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="d4584-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="d4584-115">To polecenie umożliwia pobieranie wszystkich subskrypcji w bieżącej dzierżawie autoryzowanych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d4584-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="d4584-116">Przykład 4: Zmienianie bieżącego kontekstu w celu korzystania z określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d4584-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="d4584-117">To polecenie pobiera określoną subskrypcję, a następnie ustawia bieżący kontekst, aby go używać.</span><span class="sxs-lookup"><span data-stu-id="d4584-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="d4584-118">Wszystkie kolejne polecenia cmdlet w tej sesji domyślnie używają nowego abonamentu (subskrypcja contoso 1).</span><span class="sxs-lookup"><span data-stu-id="d4584-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="d4584-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4584-119">PARAMETERS</span></span>

### <span data-ttu-id="d4584-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4584-120">-AsJob</span></span>
<span data-ttu-id="d4584-121">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="d4584-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d4584-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4584-122">-DefaultProfile</span></span>
<span data-ttu-id="d4584-123">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d4584-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4584-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d4584-124">-SubscriptionId</span></span>
<span data-ttu-id="d4584-125">Określa identyfikator subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="d4584-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="d4584-126">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="d4584-126">-SubscriptionName</span></span>
<span data-ttu-id="d4584-127">Określa nazwę subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="d4584-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="d4584-128">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="d4584-128">-TenantId</span></span>
<span data-ttu-id="d4584-129">Określa identyfikator dzierżawy, który zawiera abonamenty do pobrania.</span><span class="sxs-lookup"><span data-stu-id="d4584-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="d4584-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4584-130">CommonParameters</span></span>
<span data-ttu-id="d4584-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4584-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4584-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4584-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4584-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4584-133">INPUTS</span></span>

### <span data-ttu-id="d4584-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d4584-134">System.String</span></span>

## <span data-ttu-id="d4584-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4584-135">OUTPUTS</span></span>

### <span data-ttu-id="d4584-136">Microsoft. Azure. Commands. profile. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="d4584-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="d4584-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4584-137">NOTES</span></span>

## <span data-ttu-id="d4584-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4584-138">RELATED LINKS</span></span>