---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/new-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/New-AzSubscription.md
ms.openlocfilehash: 167678bfe84117cdc53e9e90b520abe24fed4b92
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220212"
---
# <span data-ttu-id="4c27b-101">New-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="4c27b-101">New-AzSubscription</span></span>

## <span data-ttu-id="4c27b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c27b-102">SYNOPSIS</span></span>
<span data-ttu-id="4c27b-103">Tworzy subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4c27b-103">Creates an Azure subscription.</span></span>

## <span data-ttu-id="4c27b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c27b-104">SYNTAX</span></span>

```
New-AzSubscription -EnrollmentAccountObjectId <String> [[-Name] <String>] -OfferType <String>
 [-OwnerObjectId <String[]>] [-OwnerSignInName <String[]>] [-OwnerApplicationId <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c27b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4c27b-105">DESCRIPTION</span></span>
<span data-ttu-id="4c27b-106">Polecenie cmdlet **New-AzSubscription** tworzy subskrypcję platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4c27b-106">The **New-AzSubscription** cmdlet creates an Azure subscription.</span></span>

## <span data-ttu-id="4c27b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c27b-107">EXAMPLES</span></span>

### <span data-ttu-id="4c27b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c27b-108">Example 1</span></span>
```
PS C:\> New-AzSubscription -Name "My Subscription" -EnrollmentAccountObjectId ((Get-AzEnrollmentAccount)[0].ObjectId) -OfferType MS-AZR-0017P

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="4c27b-109">Tworzy subskrypcję platformy Azure na podstawie określonego konta rejestracji z określonym typem oferty.</span><span class="sxs-lookup"><span data-stu-id="4c27b-109">Creates an Azure subscription under the specified enrollment account with the specified offer type.</span></span>

## <span data-ttu-id="4c27b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c27b-110">PARAMETERS</span></span>

### <span data-ttu-id="4c27b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c27b-111">-AsJob</span></span>
<span data-ttu-id="4c27b-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4c27b-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c27b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c27b-113">-DefaultProfile</span></span>
<span data-ttu-id="4c27b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c27b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c27b-115">-EnrollmentAccountObjectId</span><span class="sxs-lookup"><span data-stu-id="4c27b-115">-EnrollmentAccountObjectId</span></span>
<span data-ttu-id="4c27b-116">Nazwa konta rejestracji do użycia podczas tworzenia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4c27b-116">Name of the enrollment account to use when creating the subscription.</span></span>

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

### <span data-ttu-id="4c27b-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c27b-117">-Name</span></span>
<span data-ttu-id="4c27b-118">Nazwa subskrypcji, którą należy utworzyć.</span><span class="sxs-lookup"><span data-stu-id="4c27b-118">The name of the subscription to create.</span></span>

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

### <span data-ttu-id="4c27b-119">-Offertype</span><span class="sxs-lookup"><span data-stu-id="4c27b-119">-OfferType</span></span>
<span data-ttu-id="4c27b-120">Typ oferty, który ma być używany podczas tworzenia subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4c27b-120">The type of offer to use when creating the subscription.</span></span>

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

### <span data-ttu-id="4c27b-121">-OwnerApplicationId</span><span class="sxs-lookup"><span data-stu-id="4c27b-121">-OwnerApplicationId</span></span>
<span data-ttu-id="4c27b-122">Nazwy SPN aplikacji, którym ma być udzielony dostęp właścicielowi subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4c27b-122">The app SPN(s) to be granted Owner access to the subscription.</span></span>

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

### <span data-ttu-id="4c27b-123">-OwnerObjectId</span><span class="sxs-lookup"><span data-stu-id="4c27b-123">-OwnerObjectId</span></span>
<span data-ttu-id="4c27b-124">Użytkownik (y) lub identyfikatory obiektów grup, którym ma być udzielony dostęp właścicielowi subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4c27b-124">The user(s) or group object(s) id(s) to be granted Owner access to the subscription.</span></span>

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

### <span data-ttu-id="4c27b-125">-OwnerSignInName</span><span class="sxs-lookup"><span data-stu-id="4c27b-125">-OwnerSignInName</span></span>
<span data-ttu-id="4c27b-126">Użytkownik, któremu udzielono prawa dostępu właściciela do abonamentu.</span><span class="sxs-lookup"><span data-stu-id="4c27b-126">The user(s) to be granted Owner access to the subscription.</span></span>

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

### <span data-ttu-id="4c27b-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c27b-127">-Confirm</span></span>
<span data-ttu-id="4c27b-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c27b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c27b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c27b-129">-WhatIf</span></span>
<span data-ttu-id="4c27b-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c27b-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4c27b-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4c27b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c27b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c27b-132">CommonParameters</span></span>
<span data-ttu-id="4c27b-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c27b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c27b-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c27b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c27b-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c27b-135">INPUTS</span></span>

### <span data-ttu-id="4c27b-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4c27b-136">None</span></span>

## <span data-ttu-id="4c27b-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c27b-137">OUTPUTS</span></span>

### <span data-ttu-id="4c27b-138">Microsoft. Azure. Commands. Subscription. models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="4c27b-138">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="4c27b-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c27b-139">NOTES</span></span>

## <span data-ttu-id="4c27b-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c27b-140">RELATED LINKS</span></span>
