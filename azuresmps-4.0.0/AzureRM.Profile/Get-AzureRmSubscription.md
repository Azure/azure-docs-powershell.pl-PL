---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 13dd14f59b28e3b5730f207c675771e1275392d3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523398"
---
# <span data-ttu-id="e9abf-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="e9abf-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="e9abf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9abf-102">SYNOPSIS</span></span>
<span data-ttu-id="e9abf-103">Uzyskaj subskrypcje, do których bieżące konto może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="e9abf-103">Get subscriptions that the current account can access.</span></span>

## <span data-ttu-id="e9abf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9abf-104">SYNTAX</span></span>

### <span data-ttu-id="e9abf-105">ListByIdInTenant (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e9abf-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [<CommonParameters>]
```

### <span data-ttu-id="e9abf-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="e9abf-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [<CommonParameters>]
```

## <span data-ttu-id="e9abf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e9abf-107">DESCRIPTION</span></span>
<span data-ttu-id="e9abf-108">Polecenie cmdlet Get-AzureRmSubscription Pobiera identyfikator subskrypcji, nazwę subskrypcji i dzierżawę domową dla subskrypcji, do których może uzyskać dostęp bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="e9abf-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="e9abf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9abf-109">EXAMPLES</span></span>

### <span data-ttu-id="e9abf-110">Przykład 1. Uzyskaj wszystkie subskrypcje we wszystkich dzierżawach</span><span class="sxs-lookup"><span data-stu-id="e9abf-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription -All

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="e9abf-111">To polecenie pobiera wszystkie subskrypcje wszystkich dzierżawców autoryzowanych jako bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="e9abf-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="e9abf-112">Przykład 2: uzyskiwanie wszystkich subskrypcji dla konkretnego dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e9abf-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e9abf-113">Wyświetlanie wszystkich subskrypcji w danej dzierżawie autoryzowanych dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="e9abf-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="e9abf-114">Przykład 3: uzyskiwanie wszystkich subskrypcji w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="e9abf-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="e9abf-115">To polecenie umożliwia pobieranie wszystkich subskrypcji w bieżącej dzierżawie autoryzowanych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e9abf-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="e9abf-116">Przykład 4: Zmienianie bieżącego kontekstu w celu korzystania z określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e9abf-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="e9abf-117">To polecenie pobiera określoną subskrypcję, a następnie ustawia bieżący kontekst, aby go używać.</span><span class="sxs-lookup"><span data-stu-id="e9abf-117">This command gets the specified subscription, and then sets the current context to use it.</span></span>
<span data-ttu-id="e9abf-118">Wszystkie kolejne polecenia cmdlet w tej sesji domyślnie używają nowego abonamentu (subskrypcja contoso 1).</span><span class="sxs-lookup"><span data-stu-id="e9abf-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="e9abf-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9abf-119">PARAMETERS</span></span>

### <span data-ttu-id="e9abf-120">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e9abf-120">-SubscriptionId</span></span>
<span data-ttu-id="e9abf-121">Określa identyfikator subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="e9abf-121">Specifies the ID of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByIdInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9abf-122">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="e9abf-122">-SubscriptionName</span></span>
<span data-ttu-id="e9abf-123">Określa nazwę subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="e9abf-123">Specifies the name of the subscription to get.</span></span>

```yaml
Type: String
Parameter Sets: ListByNameInTenant
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9abf-124">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="e9abf-124">-TenantId</span></span>
<span data-ttu-id="e9abf-125">Określa identyfikator dzierżawy, który zawiera abonamenty do pobrania.</span><span class="sxs-lookup"><span data-stu-id="e9abf-125">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9abf-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9abf-126">CommonParameters</span></span>
<span data-ttu-id="e9abf-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9abf-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9abf-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9abf-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9abf-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9abf-129">INPUTS</span></span>

## <span data-ttu-id="e9abf-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9abf-130">OUTPUTS</span></span>

### <span data-ttu-id="e9abf-131">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="e9abf-131">PSAzureSubscription</span></span>

## <span data-ttu-id="e9abf-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9abf-132">NOTES</span></span>

## <span data-ttu-id="e9abf-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9abf-133">RELATED LINKS</span></span>

