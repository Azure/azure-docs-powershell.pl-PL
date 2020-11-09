---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: e3400ea600ed2891101a94f9ec1a7853326a7c04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316812"
---
# <span data-ttu-id="cb2de-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb2de-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="cb2de-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb2de-102">SYNOPSIS</span></span>
<span data-ttu-id="cb2de-103">Pobiera abonamenty.</span><span class="sxs-lookup"><span data-stu-id="cb2de-103">Gets subscriptions.</span></span>

## <span data-ttu-id="cb2de-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb2de-104">SYNTAX</span></span>

### <span data-ttu-id="cb2de-105">GetAllSubscriptions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cb2de-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cb2de-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cb2de-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2de-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="cb2de-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2de-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="cb2de-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2de-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="cb2de-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb2de-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="cb2de-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb2de-111">Opis</span><span class="sxs-lookup"><span data-stu-id="cb2de-111">DESCRIPTION</span></span>
<span data-ttu-id="cb2de-112">Polecenie cmdlet **Get-AzApiManagementSubscription** pobiera określoną subskrypcję lub wszystkie subskrypcje, jeśli nie określono abonamentu.</span><span class="sxs-lookup"><span data-stu-id="cb2de-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="cb2de-113">Klucze nie zostaną uwzględnione w szczegółach wyników.</span><span class="sxs-lookup"><span data-stu-id="cb2de-113">Keys will not be included into result details.</span></span> <span data-ttu-id="cb2de-114">Aby uzyskać klucze, użyj funkcji **Get-AzApiManagementSubscriptionKey**.</span><span class="sxs-lookup"><span data-stu-id="cb2de-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="cb2de-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb2de-115">EXAMPLES</span></span>

### <span data-ttu-id="cb2de-116">Przykład 1: Uzyskaj wszystkie subskrypcje</span><span class="sxs-lookup"><span data-stu-id="cb2de-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="cb2de-117">To polecenie pobiera wszystkie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="cb2de-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="cb2de-118">Przykład 2: uzyskiwanie abonamentu o określonym IDENTYFIKATORze</span><span class="sxs-lookup"><span data-stu-id="cb2de-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="cb2de-119">To polecenie pobiera abonament według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="cb2de-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="cb2de-120">Przykład 3: uzyskiwanie wszystkich subskrypcji dla użytkownika</span><span class="sxs-lookup"><span data-stu-id="cb2de-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="cb2de-121">To polecenie uzyskuje subskrypcje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cb2de-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="cb2de-122">Przykład 4: uzyskiwanie wszystkich subskrypcji produktu</span><span class="sxs-lookup"><span data-stu-id="cb2de-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="cb2de-123">To polecenie pobiera wszystkie subskrypcje produktu.</span><span class="sxs-lookup"><span data-stu-id="cb2de-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="cb2de-124">Przykład 5: uzyskiwanie wszystkich subskrypcji dla zakresu</span><span class="sxs-lookup"><span data-stu-id="cb2de-124">Example 5: Get all subscriptions for a Scope</span></span>
```powershell
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

<span data-ttu-id="cb2de-125">To polecenie pobiera wszystkie subskrypcje skonfigurowane dla globalnego zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="cb2de-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="cb2de-126">Przykład 6: uzyskiwanie wszystkich subskrypcji produktu i zakresu użytkowników</span><span class="sxs-lookup"><span data-stu-id="cb2de-126">Example 6: Get all subscriptions for a product and user scope</span></span>
```powershell
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

<span data-ttu-id="cb2de-127">To polecenie pobiera wszystkie subskrypcje skonfigurowane dla globalnego zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="cb2de-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="cb2de-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb2de-128">PARAMETERS</span></span>

### <span data-ttu-id="cb2de-129">-Context</span><span class="sxs-lookup"><span data-stu-id="cb2de-129">-Context</span></span>
<span data-ttu-id="cb2de-130">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="cb2de-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="cb2de-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb2de-131">-DefaultProfile</span></span>
<span data-ttu-id="cb2de-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb2de-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb2de-133">-ProductId</span><span class="sxs-lookup"><span data-stu-id="cb2de-133">-ProductId</span></span>
<span data-ttu-id="cb2de-134">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="cb2de-134">Specifies a product identifier.</span></span>
<span data-ttu-id="cb2de-135">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora produktu.</span><span class="sxs-lookup"><span data-stu-id="cb2de-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="cb2de-136">-Zakres</span><span class="sxs-lookup"><span data-stu-id="cb2de-136">-Scope</span></span>
<span data-ttu-id="cb2de-137">Identyfikator zakresu.</span><span class="sxs-lookup"><span data-stu-id="cb2de-137">Scope identifier.</span></span> <span data-ttu-id="cb2de-138">Zakres subskrypcji, niezależnie od tego, czy jest to zakres API/apis/{apiId}, czy zakres/products/{productId} lub globalny zakres interfejsu API/Apis czy globalny zakres/.</span><span class="sxs-lookup"><span data-stu-id="cb2de-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="cb2de-139">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="cb2de-139">-SubscriptionId</span></span>
<span data-ttu-id="cb2de-140">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="cb2de-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="cb2de-141">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie abonamentu o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="cb2de-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="cb2de-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="cb2de-142">-UserId</span></span>
<span data-ttu-id="cb2de-143">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cb2de-143">Specifies a user identifier.</span></span>
<span data-ttu-id="cb2de-144">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cb2de-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="cb2de-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb2de-145">CommonParameters</span></span>
<span data-ttu-id="cb2de-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb2de-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb2de-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cb2de-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb2de-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb2de-148">INPUTS</span></span>

### <span data-ttu-id="cb2de-149">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="cb2de-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="cb2de-150">System. String</span><span class="sxs-lookup"><span data-stu-id="cb2de-150">System.String</span></span>

## <span data-ttu-id="cb2de-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb2de-151">OUTPUTS</span></span>

### <span data-ttu-id="cb2de-152">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb2de-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="cb2de-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb2de-153">NOTES</span></span>

## <span data-ttu-id="cb2de-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb2de-154">RELATED LINKS</span></span>

[<span data-ttu-id="cb2de-155">Nowe — AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb2de-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="cb2de-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb2de-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="cb2de-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="cb2de-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


