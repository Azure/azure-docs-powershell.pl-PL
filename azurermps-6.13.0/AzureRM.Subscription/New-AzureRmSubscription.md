---
external help file: Microsoft.Azure.Commands.Subscription.dll-Help.xml
Module Name: AzureRM.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription/new-azurermsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscription.md
ms.openlocfilehash: cc88f762f1e965eb4e46462f7d43074fa3fe4646
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553407"
---
# <span data-ttu-id="9c581-101">New-AzureRmSubscription</span><span class="sxs-lookup"><span data-stu-id="9c581-101">New-AzureRmSubscription</span></span>

## <span data-ttu-id="9c581-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c581-102">SYNOPSIS</span></span>
<span data-ttu-id="9c581-103">Tworzy subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9c581-103">Creates an Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c581-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c581-104">SYNTAX</span></span>

```
New-AzureRmSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c581-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9c581-105">DESCRIPTION</span></span>
<span data-ttu-id="9c581-106">Polecenie cmdlet **New-AzureRmSubscription** tworzy subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9c581-106">The **New-AzureRmSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="9c581-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c581-107">EXAMPLES</span></span>

### <span data-ttu-id="9c581-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9c581-108">Example 1</span></span>
```
PS C:\> New-AzureRmSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzureRmEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="9c581-109">Tworzy subskrypcję platformy Azure na podstawie określonego konta rejestracji z określonym typem oferty.</span><span class="sxs-lookup"><span data-stu-id="9c581-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="9c581-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c581-110">PARAMETERS</span></span>

### <span data-ttu-id="9c581-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c581-111">-AsJob</span></span>
<span data-ttu-id="9c581-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9c581-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c581-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c581-113">-DefaultProfile</span></span>
<span data-ttu-id="9c581-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c581-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c581-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="9c581-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="9c581-116">Nazwa konta rejestracji do użycia podczas tworzenia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9c581-116">Name of the enrollment account to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c581-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c581-117">-Name</span></span>
<span data-ttu-id="9c581-118">Nazwa subskrypcji, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="9c581-118">The name of the subscription to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c581-119">-Offertype</span><span class="sxs-lookup"><span data-stu-id="9c581-119">-OfferType</span></span>
<span data-ttu-id="9c581-120">Typ oferty, który ma być używany podczas tworzenia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9c581-120">The type of offer to use when creating the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c581-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="9c581-121">-OwnerApplicationId</span></span>
<span data-ttu-id="9c581-122">Nazwy SPN aplikacji, którym ma być udzielony dostęp właścicielowi subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9c581-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerSPN, OwnerServicePrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c581-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="9c581-123">-OwnerObjectId</span></span>
<span data-ttu-id="9c581-124">Użytkownik (y) lub identyfikatory obiektów grup, którym ma być udzielony dostęp właścicielowi subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9c581-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerId, OwnerPrincipalId

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c581-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="9c581-125">-OwnerSignInName</span></span>
<span data-ttu-id="9c581-126">Użytkownik, któremu udzielono prawa dostępu właściciela do abonamentu.</span><span class="sxs-lookup"><span data-stu-id="9c581-126">The user(s) to be granted Owner access to the subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: OwnerEmail, OwnerUserPrincipalName

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c581-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c581-127">-Confirm</span></span>
<span data-ttu-id="9c581-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c581-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c581-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c581-129">-WhatIf</span></span>
<span data-ttu-id="9c581-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c581-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c581-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c581-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c581-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c581-132">CommonParameters</span></span>
<span data-ttu-id="9c581-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c581-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c581-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c581-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c581-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c581-135">INPUTS</span></span>

### <span data-ttu-id="9c581-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9c581-136">None</span></span>

## <span data-ttu-id="9c581-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c581-137">OUTPUTS</span></span>

### <span data-ttu-id="9c581-138">Microsoft. Azure. Commands. Subscription. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="9c581-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="9c581-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c581-139">NOTES</span></span>

## <span data-ttu-id="9c581-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c581-140">RELATED LINKS</span></span>
