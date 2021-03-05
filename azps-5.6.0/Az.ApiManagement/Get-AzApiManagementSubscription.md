---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 26e555be760a71defc7f21f5ffc84cada7a21d04
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012858"
---
# <span data-ttu-id="9e1d2-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9e1d2-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="9e1d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e1d2-102">SYNOPSIS</span></span>
<span data-ttu-id="9e1d2-103">Otrzymuje subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-103">Gets subscriptions.</span></span>

## <span data-ttu-id="9e1d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9e1d2-104">SYNTAX</span></span>

### <span data-ttu-id="9e1d2-105">GetAllSubscriptions (Default)</span><span class="sxs-lookup"><span data-stu-id="9e1d2-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e1d2-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e1d2-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e1d2-107">GetByProductIdAndUser</span><span class="sxs-lookup"><span data-stu-id="9e1d2-107">GetByProductIdAndUser</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -UserId <String> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e1d2-108">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="9e1d2-108">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e1d2-109">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="9e1d2-109">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e1d2-110">GetByScope</span><span class="sxs-lookup"><span data-stu-id="9e1d2-110">GetByScope</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> -Scope <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9e1d2-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="9e1d2-111">DESCRIPTION</span></span>
<span data-ttu-id="9e1d2-112">Polecenie **cmdlet Get-AzApiManagementSubscription** otrzymuje określoną subskrypcję lub wszystkie subskrypcje, jeśli nie określono subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-112">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>
<span data-ttu-id="9e1d2-113">Klucze nie zostaną uwzględnione w szczegółach wyników.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-113">Keys will not be included into result details.</span></span> <span data-ttu-id="9e1d2-114">Aby uzyskać klucze, użyj przycisku **Get-AzApiManagementSubscriptionKey.**</span><span class="sxs-lookup"><span data-stu-id="9e1d2-114">To get keys, use **Get-AzApiManagementSubscriptionKey**.</span></span>

## <span data-ttu-id="9e1d2-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9e1d2-115">EXAMPLES</span></span>

### <span data-ttu-id="9e1d2-116">Przykład 1. Uzyskiwanie wszystkich subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9e1d2-116">Example 1: Get all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="9e1d2-117">To polecenie otrzymuje wszystkie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-117">This command gets all subscriptions.</span></span>

### <span data-ttu-id="9e1d2-118">Przykład 2. Uzyskiwanie subskrypcji o określonym identyfikatorze</span><span class="sxs-lookup"><span data-stu-id="9e1d2-118">Example 2: Get a subscription with a specified ID</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="9e1d2-119">To polecenie otrzymuje subskrypcję według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-119">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="9e1d2-120">Przykład 3. Uzyskiwanie wszystkich subskrypcji dla użytkownika</span><span class="sxs-lookup"><span data-stu-id="9e1d2-120">Example 3: Get all subscriptions for a user</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="9e1d2-121">To polecenie pobiera subskrypcje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-121">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="9e1d2-122">Przykład 4. Uzyskiwanie wszystkich subskrypcji produktu</span><span class="sxs-lookup"><span data-stu-id="9e1d2-122">Example 4: Get all subscriptions for a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="9e1d2-123">To polecenie pobiera wszystkie subskrypcje danego produktu.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-123">This command gets all subscriptions for the product.</span></span>

### <span data-ttu-id="9e1d2-124">Przykład 5. Uzyskiwanie wszystkich subskrypcji dla zakresu</span><span class="sxs-lookup"><span data-stu-id="9e1d2-124">Example 5: Get all subscriptions for a Scope</span></span>
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

<span data-ttu-id="9e1d2-125">To polecenie pobiera wszystkie subskrypcje, które są skonfigurowane dla globalnego zakresu interfejsu API</span><span class="sxs-lookup"><span data-stu-id="9e1d2-125">This command gets all subscriptions which are configured for global api scope</span></span>

### <span data-ttu-id="9e1d2-126">Przykład 6. Uzyskiwanie wszystkich subskrypcji dla produktu i zakresu użytkownika</span><span class="sxs-lookup"><span data-stu-id="9e1d2-126">Example 6: Get all subscriptions for a product and user scope</span></span>
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

<span data-ttu-id="9e1d2-127">To polecenie pobiera wszystkie subskrypcje, które są skonfigurowane dla globalnego zakresu interfejsu API</span><span class="sxs-lookup"><span data-stu-id="9e1d2-127">This command gets all subscriptions which are configured for global api scope</span></span>

## <span data-ttu-id="9e1d2-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e1d2-128">PARAMETERS</span></span>

### <span data-ttu-id="9e1d2-129">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9e1d2-129">-Context</span></span>
<span data-ttu-id="9e1d2-130">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="9e1d2-130">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9e1d2-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e1d2-131">-DefaultProfile</span></span>
<span data-ttu-id="9e1d2-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e1d2-133">- ProductId</span><span class="sxs-lookup"><span data-stu-id="9e1d2-133">-ProductId</span></span>
<span data-ttu-id="9e1d2-134">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-134">Specifies a product identifier.</span></span>
<span data-ttu-id="9e1d2-135">Jeśli zostanie określone, to polecenie cmdlet znajdzie wszystkie subskrypcje według identyfikatora produktu.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-135">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="9e1d2-136">— Zakres</span><span class="sxs-lookup"><span data-stu-id="9e1d2-136">-Scope</span></span>
<span data-ttu-id="9e1d2-137">Identyfikator zakresu.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-137">Scope identifier.</span></span> <span data-ttu-id="9e1d2-138">Zakres subskrypcji, czy to zakres api /apis/{apiId} lub zakres produktu /products/{productId}, zakres /apis lub zakres globalny /.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-138">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span>

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

### <span data-ttu-id="9e1d2-139">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9e1d2-139">-SubscriptionId</span></span>
<span data-ttu-id="9e1d2-140">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-140">Specifies a subscription identifier.</span></span>
<span data-ttu-id="9e1d2-141">Jeśli zostanie określone, to polecenie cmdlet znajdzie subskrypcję za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-141">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="9e1d2-142">-UserId</span><span class="sxs-lookup"><span data-stu-id="9e1d2-142">-UserId</span></span>
<span data-ttu-id="9e1d2-143">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-143">Specifies a user identifier.</span></span>
<span data-ttu-id="9e1d2-144">Jeśli zostanie określone, to polecenie cmdlet znajdzie wszystkie subskrypcje według identyfikatora użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-144">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="9e1d2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e1d2-145">CommonParameters</span></span>
<span data-ttu-id="9e1d2-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e1d2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e1d2-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e1d2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e1d2-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e1d2-148">INPUTS</span></span>

### <span data-ttu-id="9e1d2-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9e1d2-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e1d2-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9e1d2-150">System.String</span></span>

## <span data-ttu-id="9e1d2-151">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9e1d2-151">OUTPUTS</span></span>

### <span data-ttu-id="9e1d2-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9e1d2-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="9e1d2-153">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9e1d2-153">NOTES</span></span>

## <span data-ttu-id="9e1d2-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9e1d2-154">RELATED LINKS</span></span>

[<span data-ttu-id="9e1d2-155">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9e1d2-155">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="9e1d2-156">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9e1d2-156">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="9e1d2-157">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="9e1d2-157">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


