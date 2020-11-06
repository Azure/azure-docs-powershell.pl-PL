---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 09d51ccf8d4ebdc387977d480be606bf9ed9d9df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551687"
---
# <span data-ttu-id="0d2b8-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="0d2b8-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="0d2b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d2b8-102">SYNOPSIS</span></span>
<span data-ttu-id="0d2b8-103">Uzyskaj subskrypcje, do których bieżące konto może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d2b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d2b8-104">SYNTAX</span></span>

### <span data-ttu-id="0d2b8-105">ListByIdInTenant (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0d2b8-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d2b8-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="0d2b8-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d2b8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0d2b8-107">DESCRIPTION</span></span>
<span data-ttu-id="0d2b8-108">Polecenie cmdlet Get-AzureRmSubscription Pobiera identyfikator subskrypcji, nazwę subskrypcji i dzierżawę domową dla subskrypcji, do których może uzyskać dostęp bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="0d2b8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d2b8-109">EXAMPLES</span></span>

### <span data-ttu-id="0d2b8-110">Przykład 1. Uzyskaj wszystkie subskrypcje we wszystkich dzierżawach</span><span class="sxs-lookup"><span data-stu-id="0d2b8-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : xxxx-xxxx-xxxx-xxxx
TenantId : yyyy-yyyy-yyyy-yyyy
State    : Enabled
```

<span data-ttu-id="0d2b8-111">To polecenie pobiera wszystkie subskrypcje wszystkich dzierżawców autoryzowanych jako bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="0d2b8-112">Przykład 2: uzyskiwanie wszystkich subskrypcji dla konkretnego dzierżawy</span><span class="sxs-lookup"><span data-stu-id="0d2b8-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="0d2b8-113">Wyświetlanie wszystkich subskrypcji w danej dzierżawie autoryzowanych dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="0d2b8-114">Przykład 3: uzyskiwanie wszystkich subskrypcji w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="0d2b8-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name     : Contoso Subscription 1
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled

Name     : Contoso Subscription 2
Id       : yyyy-yyyy-yyyy-yyyy
TenantId : xxxx-xxxx-xxxx-xxxx
State    : Enabled
```

<span data-ttu-id="0d2b8-115">To polecenie umożliwia pobieranie wszystkich subskrypcji w bieżącej dzierżawie autoryzowanych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="0d2b8-116">Przykład 4: Zmienianie bieżącego kontekstu w celu korzystania z określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0d2b8-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Environment           : AzureCloud
Account               : user@example.com
TenantId              : yyyy-yyyy-yyyy-yyyy
SubscriptionId        : xxxx-xxxx-xxxx-xxxx
SubscriptionName      : Contoso Subscription 1
CurrentStorageAccount :
```

<span data-ttu-id="0d2b8-117">To polecenie pobiera określoną subskrypcję, a następnie ustawia bieżący kontekst, aby go używać.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="0d2b8-118">Wszystkie kolejne polecenia cmdlet w tej sesji domyślnie używają nowego abonamentu (subskrypcja contoso 1).</span><span class="sxs-lookup"><span data-stu-id="0d2b8-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="0d2b8-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d2b8-119">PARAMETERS</span></span>

### <span data-ttu-id="0d2b8-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d2b8-120">-AsJob</span></span>
<span data-ttu-id="0d2b8-121">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-121">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d2b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d2b8-122">-DefaultProfile</span></span>
<span data-ttu-id="0d2b8-123">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0d2b8-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d2b8-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0d2b8-124">-SubscriptionId</span></span>
<span data-ttu-id="0d2b8-125">Określa identyfikator subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="0d2b8-126">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="0d2b8-126">-SubscriptionName</span></span>
<span data-ttu-id="0d2b8-127">Określa nazwę subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="0d2b8-128">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="0d2b8-128">-TenantId</span></span>
<span data-ttu-id="0d2b8-129">Określa identyfikator dzierżawy, który zawiera abonamenty do pobrania.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="0d2b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d2b8-130">CommonParameters</span></span>
<span data-ttu-id="0d2b8-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d2b8-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d2b8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d2b8-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d2b8-133">INPUTS</span></span>

### <span data-ttu-id="0d2b8-134">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0d2b8-134">None</span></span>
<span data-ttu-id="0d2b8-135">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0d2b8-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0d2b8-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d2b8-136">OUTPUTS</span></span>

### <span data-ttu-id="0d2b8-137">PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="0d2b8-137">PSAzureSubscription</span></span>

## <span data-ttu-id="0d2b8-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d2b8-138">NOTES</span></span>

## <span data-ttu-id="0d2b8-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d2b8-139">RELATED LINKS</span></span>

