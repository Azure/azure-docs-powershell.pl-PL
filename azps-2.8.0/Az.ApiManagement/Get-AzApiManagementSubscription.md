---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 13ca3444a48d79b3708042f6cf8fd0229f80676a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707060"
---
# <span data-ttu-id="e62c3-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e62c3-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="e62c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e62c3-102">SYNOPSIS</span></span>
<span data-ttu-id="e62c3-103">Pobiera abonamenty.</span><span class="sxs-lookup"><span data-stu-id="e62c3-103">Gets subscriptions.</span></span>

## <span data-ttu-id="e62c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e62c3-104">SYNTAX</span></span>

### <span data-ttu-id="e62c3-105">GetAllSubscriptions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e62c3-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e62c3-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e62c3-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e62c3-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="e62c3-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e62c3-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="e62c3-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e62c3-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="e62c3-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e62c3-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="e62c3-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e62c3-111">Opis</span><span class="sxs-lookup"><span data-stu-id="e62c3-111">DESCRIPTION</span></span>
<span data-ttu-id="e62c3-112">Polecenie cmdlet **Get-AzApiManagementSubscription** pobiera określoną subskrypcję lub wszystkie subskrypcje, jeśli nie określono abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e62c3-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="e62c3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e62c3-113">EXAMPLES</span></span>

### <span data-ttu-id="e62c3-114">Przykład 1: Uzyskaj wszystkie subskrypcje</span><span class="sxs-lookup"><span data-stu-id="e62c3-114">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="e62c3-115">To polecenie pobiera wszystkie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="e62c3-115">This command gets all subscriptions.</span></span>

### <span data-ttu-id="e62c3-116">Przykład 2: uzyskiwanie abonamentu o określonym IDENTYFIKATORze</span><span class="sxs-lookup"><span data-stu-id="e62c3-116">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="e62c3-117">To polecenie pobiera abonament według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="e62c3-117">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="e62c3-118">Przykład 3: uzyskiwanie wszystkich subskrypcji dla użytkownika</span><span class="sxs-lookup"><span data-stu-id="e62c3-118">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="e62c3-119">To polecenie uzyskuje subskrypcje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e62c3-119">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="e62c3-120">Przykład 4: uzyskiwanie wszystkich subskrypcji produktu</span><span class="sxs-lookup"><span data-stu-id="e62c3-120">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="e62c3-121">To polecenie pobiera wszystkie subskrypcje produktu.</span><span class="sxs-lookup"><span data-stu-id="e62c3-121">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="e62c3-122">Przykład 5: uzyskiwanie wszystkich subskrypcji dla zakresu</span><span class="sxs-lookup"><span data-stu-id="e62c3-122">Example 5: Get all subscriptions for a Scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -Scope "/apis"

SubscriptionId    : allApScope
UserId            :
OwnerId           :
ProductId         :
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/apis
Name              : All Api Scope
State             : Active
CreatedDate       : 6/18/2019 5:53:49 PM
StartDate         :
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
StateComment      :
AllowTracing      : False
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/allApScope
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="e62c3-123">To polecenie pobiera wszystkie subskrypcje skonfigurowane dla globalnego zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="e62c3-123">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="e62c3-124">Przykład 5: uzyskiwanie wszystkich subskrypcji produktu i zakresu użytkowników</span><span class="sxs-lookup"><span data-stu-id="e62c3-124">Example 5: Get all subscriptions for a product and user scope</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId 59b872f28a82740f547e6270 -UserId 1

SubscriptionId    : 59b872f38a82741750c8da56
UserId            : 1
OwnerId           : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/users/1
ProductId         : 59b872f28a82740f547e6270
Scope             : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/products/59b872f28a82740f547e6270
Name              :
State             : Active
CreatedDate       : 9/12/2017 11:51:15 PM
StartDate         : 9/12/2017 12:00:00 AM
ExpirationDate    :
EndDate           :
NotificationDate  :
PrimaryKey        : 7e64ef904b194706835febf87f729bb0
SecondaryKey      : 0354fccef73e43feb82e5c5da17674d5
StateComment      :
AllowTracing      : True
Id                : /subscriptions/subid/resourceGroups/Api-Default-East-US/providers/Microsoft.ApiManagement/service/contoso/subscriptions/59b872f38a82741750c8da56
ResourceGroupName : Api-Default-East-US
ServiceName       : contoso
```

<span data-ttu-id="e62c3-125">To polecenie pobiera wszystkie subskrypcje skonfigurowane dla globalnego zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="e62c3-125">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="e62c3-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e62c3-126">PARAMETERS</span></span>

### <span data-ttu-id="e62c3-127">-Context</span><span class="sxs-lookup"><span data-stu-id="e62c3-127">-Context</span></span>
<span data-ttu-id="e62c3-128">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e62c3-128">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e62c3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e62c3-129">-DefaultProfile</span></span>
<span data-ttu-id="e62c3-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e62c3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e62c3-131">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e62c3-131">-ProductId</span></span>
<span data-ttu-id="e62c3-132">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="e62c3-132">Specifies a product identifier.</span></span>
<span data-ttu-id="e62c3-133">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora produktu.</span><span class="sxs-lookup"><span data-stu-id="e62c3-133">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62c3-134">-Zakres</span><span class="sxs-lookup"><span data-stu-id="e62c3-134">-Scope</span></span>
<span data-ttu-id="e62c3-135">Identyfikator zakresu.</span><span class="sxs-lookup"><span data-stu-id="e62c3-135">Scope identifier.</span></span> <span data-ttu-id="e62c3-136">Zakres subskrypcji, niezależnie od tego, czy jest to zakres API/apis/{apiId}, czy zakres/products/{productId} lub globalny zakres interfejsu API/Apis czy globalny zakres/.</span><span class="sxs-lookup"><span data-stu-id="e62c3-136">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62c3-137">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e62c3-137">-SubscriptionId</span></span>
<span data-ttu-id="e62c3-138">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e62c3-138">Specifies a subscription identifier.</span></span>
<span data-ttu-id="e62c3-139">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie abonamentu o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="e62c3-139">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetBySubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62c3-140">-UserId</span><span class="sxs-lookup"><span data-stu-id="e62c3-140">-UserId</span></span>
<span data-ttu-id="e62c3-141">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e62c3-141">Specifies a user identifier.</span></span>
<span data-ttu-id="e62c3-142">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e62c3-142">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductIdAndUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByUserId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e62c3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e62c3-143">CommonParameters</span></span>
<span data-ttu-id="e62c3-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e62c3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e62c3-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e62c3-145">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e62c3-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e62c3-146">INPUTS</span></span>

### <span data-ttu-id="e62c3-147">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e62c3-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e62c3-148">System. String</span><span class="sxs-lookup"><span data-stu-id="e62c3-148">System.String</span></span>

## <span data-ttu-id="e62c3-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e62c3-149">OUTPUTS</span></span>

### <span data-ttu-id="e62c3-150">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e62c3-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="e62c3-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e62c3-151">NOTES</span></span>

## <span data-ttu-id="e62c3-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e62c3-152">RELATED LINKS</span></span>

[<span data-ttu-id="e62c3-153">Nowe — AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e62c3-153">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="e62c3-154">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e62c3-154">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="e62c3-155">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e62c3-155">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


