---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmSubscription.md
ms.openlocfilehash: 62f3e1b357c0a85f30ba4eeba6a92d9b8dfc9dd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544944"
---
# <span data-ttu-id="eaf1e-101">Get-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="eaf1e-101">Get-AzureRmSubscription</span></span>

## <span data-ttu-id="eaf1e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eaf1e-102">SYNOPSIS</span></span>
<span data-ttu-id="eaf1e-103">Uzyskaj subskrypcje, do których bieżące konto może uzyskać dostęp.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-103">Get subscriptions that the current account can access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaf1e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eaf1e-104">SYNTAX</span></span>

### <span data-ttu-id="eaf1e-105">ListByIdInTenant (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eaf1e-105">ListByIdInTenant (Default)</span></span>
```
Get-AzureRmSubscription [-SubscriptionId <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaf1e-106">ListByNameInTenant</span><span class="sxs-lookup"><span data-stu-id="eaf1e-106">ListByNameInTenant</span></span>
```
Get-AzureRmSubscription [-SubscriptionName <String>] [-TenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaf1e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eaf1e-107">DESCRIPTION</span></span>
<span data-ttu-id="eaf1e-108">Polecenie cmdlet Get-AzureRmSubscription Pobiera identyfikator subskrypcji, nazwę subskrypcji i dzierżawę domową dla subskrypcji, do których może uzyskać dostęp bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-108">The Get-AzureRmSubscription cmdlet gets the subscription ID, subscription name, and home tenant for subscriptions that the current account can access.</span></span>

## <span data-ttu-id="eaf1e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eaf1e-109">EXAMPLES</span></span>

### <span data-ttu-id="eaf1e-110">Przykład 1. Uzyskaj wszystkie subskrypcje we wszystkich dzierżawach</span><span class="sxs-lookup"><span data-stu-id="eaf1e-110">Example 1: Get all subscriptions in all tenants</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription3                      zzzz-zzzz-zzzz-zzzz     bbbb-bbbb-bbbb-bbbb             Enabled
```

<span data-ttu-id="eaf1e-111">To polecenie pobiera wszystkie subskrypcje wszystkich dzierżawców autoryzowanych jako bieżące konto.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-111">This command gets all subscriptions in all tenants that are authorized for the current account.</span></span>

### <span data-ttu-id="eaf1e-112">Przykład 2: uzyskiwanie wszystkich subskrypcji dla konkretnego dzierżawy</span><span class="sxs-lookup"><span data-stu-id="eaf1e-112">Example 2: Get all subscriptions for a specific tenant</span></span>
```
PS C:\>Get-AzureRmSubscription -TenantId "xxxx-xxxx-xxxx-xxxx"

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="eaf1e-113">Wyświetlanie wszystkich subskrypcji w danej dzierżawie autoryzowanych dla bieżącego konta.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-113">List all subscriptions in the given tenant that are authorized for the current account.</span></span>

### <span data-ttu-id="eaf1e-114">Przykład 3: uzyskiwanie wszystkich subskrypcji w bieżącej dzierżawie</span><span class="sxs-lookup"><span data-stu-id="eaf1e-114">Example 3: Get all subscriptions in the current tenant</span></span>
```
PS C:\>Get-AzureRmSubscription

Name                               Id                      TenantId                        State
----                               --                      --------                        -----
Subscription1                      yyyy-yyyy-yyyy-yyyy     aaaa-aaaa-aaaa-aaaa             Enabled
Subscription2                      xxxx-xxxx-xxxx-xxxx     aaaa-aaaa-aaaa-aaaa             Enabled
```

<span data-ttu-id="eaf1e-115">To polecenie umożliwia pobieranie wszystkich subskrypcji w bieżącej dzierżawie autoryzowanych dla bieżącego użytkownika.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-115">This command gets all subscriptions in the current tenant that are authorized for the current user.</span></span>

### <span data-ttu-id="eaf1e-116">Przykład 4: Zmienianie bieżącego kontekstu w celu korzystania z określonej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="eaf1e-116">Example 4: Change the current context to use a specific subscription</span></span>
```
PS C:\>Get-AzureRmSubscription -SubscriptionId "xxxx-xxxx-xxxx-xxxx" -TenantId "yyyy-yyyy-yyyy-yyyy" | Set-AzureRmContext

Name                                     Account             SubscriptionName    Environment         TenantId
----                                     -------             ----------------    -----------         --------
Subscription1 (xxxx-xxxx-xxxx-xxxx)      azureuser@micros... Subscription1       AzureCloud          yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="eaf1e-117">To polecenie pobiera określoną subskrypcję, a następnie ustawia bieżący kontekst, aby go używać.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-117">This command gets the specified subscription, and then sets the current context to use it.</span></span> <span data-ttu-id="eaf1e-118">Wszystkie kolejne polecenia cmdlet w tej sesji domyślnie używają nowego abonamentu (subskrypcja contoso 1).</span><span class="sxs-lookup"><span data-stu-id="eaf1e-118">All subsequent cmdlets in this session use the new subscription (Contoso Subscription 1) by default.</span></span>

## <span data-ttu-id="eaf1e-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eaf1e-119">PARAMETERS</span></span>

### <span data-ttu-id="eaf1e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eaf1e-120">-AsJob</span></span>
<span data-ttu-id="eaf1e-121">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="eaf1e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaf1e-122">-DefaultProfile</span></span>
<span data-ttu-id="eaf1e-123">Poświadczenia, dzierżawca i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eaf1e-123">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaf1e-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="eaf1e-124">-SubscriptionId</span></span>
<span data-ttu-id="eaf1e-125">Określa identyfikator subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-125">Specifies the ID of the subscription to get.</span></span>

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

### <span data-ttu-id="eaf1e-126">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="eaf1e-126">-SubscriptionName</span></span>
<span data-ttu-id="eaf1e-127">Określa nazwę subskrypcji, którą należy uzyskać.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-127">Specifies the name of the subscription to get.</span></span>

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

### <span data-ttu-id="eaf1e-128">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="eaf1e-128">-TenantId</span></span>
<span data-ttu-id="eaf1e-129">Określa identyfikator dzierżawy, który zawiera abonamenty do pobrania.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-129">Specifies the ID of the tenant that contains subscriptions to get.</span></span>

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

### <span data-ttu-id="eaf1e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaf1e-130">CommonParameters</span></span>
<span data-ttu-id="eaf1e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaf1e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaf1e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaf1e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaf1e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eaf1e-133">INPUTS</span></span>

### <span data-ttu-id="eaf1e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="eaf1e-134">System.String</span></span>

## <span data-ttu-id="eaf1e-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eaf1e-135">OUTPUTS</span></span>

### <span data-ttu-id="eaf1e-136">Microsoft. Azure. Commands. profile. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="eaf1e-136">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="eaf1e-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eaf1e-137">NOTES</span></span>

## <span data-ttu-id="eaf1e-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eaf1e-138">RELATED LINKS</span></span>
