---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 9e59fb8ce19d705fffdd52a172be2a333a3ca7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546116"
---
# <span data-ttu-id="a72a9-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="a72a9-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="a72a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a72a9-102">SYNOPSIS</span></span>
<span data-ttu-id="a72a9-103">Uzyskaj subskrypcje, do których bieżące konto może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="a72a9-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a72a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a72a9-104">SYNTAX</span></span>

### <span data-ttu-id="a72a9-105">ListByIdInTenant (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a72a9-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a72a9-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="a72a9-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a72a9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a72a9-107">DESCRIPTION</span></span>
<span data-ttu-id="a72a9-108">Polecenie cmdlet Get-AzureRmSubscription Pobiera identyfikator subskrypcji, nazwę subskrypcji i dzierżawę domową dla subskrypcji, do których może uzyskać dostęp bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="a72a9-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="a72a9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a72a9-109">EXAMPLES</span></span>

### <span data-ttu-id="a72a9-110">Przykład 1. Uzyskaj wszystkie subskrypcje we wszystkich dzierżawach</span><span class="sxs-lookup"><span data-stu-id="a72a9-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a72a9-111">To polecenie pobiera wszystkie subskrypcje wszystkich dzierżawców autoryzowanych jako bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="a72a9-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="a72a9-112">Przykład 2: uzyskiwanie wszystkich subskrypcji dla konkretnego dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a72a9-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a72a9-113">Wyświetlanie wszystkich subskrypcji w danej dzierżawie autoryzowanych dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="a72a9-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="a72a9-114">Przykład 3: uzyskiwanie wszystkich subskrypcji w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="a72a9-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Subscription Name : Contoso Subscription 1
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx

Subscription Name : Contoso Subscription 2
SubscriptionId    : yyyy-yyyy-yyyy-yyyy
TenantId          : xxxx-xxxx-xxxx-xxxx
```

<span data-ttu-id="a72a9-115">To polecenie umożliwia pobieranie wszystkich subskrypcji w bieżącej dzierżawie autoryzowanych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a72a9-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="a72a9-116">Przykład 4: Zmienianie bieżącego kontekstu w celu korzystania z określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a72a9-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Subscription Name : Contoso Subscription 1
SubscriptionId    : xxxx-xxxx-xxxx-xxxx
TenantId          : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="a72a9-117">To polecenie pobiera określoną subskrypcję, a następnie ustawia bieżący kontekst, aby go używać.</span><span class="sxs-lookup"><span data-stu-id="a72a9-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="a72a9-118">Wszystkie kolejne polecenia cmdlet w tej sesji domyślnie używają nowego abonamentu (subskrypcja contoso 1).</span><span class="sxs-lookup"><span data-stu-id="a72a9-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="a72a9-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a72a9-119">PARAMETERS</span></span>

### <span data-ttu-id="a72a9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72a9-120">-DefaultProfile</span></span>
<span data-ttu-id="a72a9-121">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a72a9-121">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a72a9-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a72a9-122">-SubscriptionId</span></span>
<span data-ttu-id="a72a9-123">Określa identyfikator subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="a72a9-123">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="a72a9-124">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="a72a9-124">-SubscriptionName</span></span>
<span data-ttu-id="a72a9-125">Określa nazwę subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="a72a9-125">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="a72a9-126">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a72a9-126">-TenantId</span></span>
<span data-ttu-id="a72a9-127">Określa identyfikator dzierżawy, który zawiera abonamenty do pobrania.</span><span class="sxs-lookup"><span data-stu-id="a72a9-127">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="a72a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72a9-128">CommonParameters</span></span>
<span data-ttu-id="a72a9-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a72a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72a9-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a72a9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72a9-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a72a9-131">INPUTS</span></span>

## <span data-ttu-id="a72a9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a72a9-132">OUTPUTS</span></span>

### <span data-ttu-id="a72a9-133">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="a72a9-133">PSAzureSubscription</span></span>

## <span data-ttu-id="a72a9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a72a9-134">NOTES</span></span>

## <span data-ttu-id="a72a9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a72a9-135">RELATED LINKS</span></span>

