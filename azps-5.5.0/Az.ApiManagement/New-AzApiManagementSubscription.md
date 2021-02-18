---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239722"
---
# <span data-ttu-id="8e6ff-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8e6ff-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="8e6ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e6ff-102">SYNOPSIS</span></span>
<span data-ttu-id="8e6ff-103">Tworzy subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-103">Creates a subscription.</span></span>

## <span data-ttu-id="8e6ff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8e6ff-104">SYNTAX</span></span>

### <span data-ttu-id="8e6ff-105">OldSubscriptionModel (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8e6ff-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e6ff-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="8e6ff-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e6ff-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8e6ff-107">DESCRIPTION</span></span>
<span data-ttu-id="8e6ff-108">Polecenie **cmdlet New-AzApiManagementSubscription** tworzy subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="8e6ff-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8e6ff-109">EXAMPLES</span></span>

### <span data-ttu-id="8e6ff-110">Przykład 1. Subskrybowanie produktu przez użytkownika</span><span class="sxs-lookup"><span data-stu-id="8e6ff-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="8e6ff-111">To polecenie subskrybuje istniejącego użytkownika do produktu.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="8e6ff-112">Przykład 2. Tworzenie subskrypcji dla wszystkich zakresów interfejsu API</span><span class="sxs-lookup"><span data-stu-id="8e6ff-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="8e6ff-113">Przykład 3. Tworzenie subskrypcji w zakresie produktu</span><span class="sxs-lookup"><span data-stu-id="8e6ff-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="8e6ff-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e6ff-114">PARAMETERS</span></span>

### <span data-ttu-id="8e6ff-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="8e6ff-115">-AllowTracing</span></span>
<span data-ttu-id="8e6ff-116">Flaga, która określa, czy śledzenie można włączyć na poziomie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="8e6ff-117">Jest to parametr opcjonalny, a wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-117">This is optional parameter and default is $null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e6ff-118">— kontekst</span><span class="sxs-lookup"><span data-stu-id="8e6ff-118">-Context</span></span>
<span data-ttu-id="8e6ff-119">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="8e6ff-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8e6ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e6ff-120">-DefaultProfile</span></span>
<span data-ttu-id="8e6ff-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e6ff-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8e6ff-122">-Name</span></span>
<span data-ttu-id="8e6ff-123">Określa nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-123">Specifies the subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e6ff-124">- Klucz Podstawowy</span><span class="sxs-lookup"><span data-stu-id="8e6ff-124">-PrimaryKey</span></span>
<span data-ttu-id="8e6ff-125">Określa klucz podstawowy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="8e6ff-126">Jeśli ten parametr nie zostanie określony, klucz zostanie wygenerowany automatycznie.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="8e6ff-127">Ten parametr musi mieć od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="8e6ff-128">- ProductId</span><span class="sxs-lookup"><span data-stu-id="8e6ff-128">-ProductId</span></span>
<span data-ttu-id="8e6ff-129">Określa identyfikator produktu, którego subskrypcję chcesz subskrybować.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-129">Specifies the ID of the product to which to subscribe.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e6ff-130">— Zakres</span><span class="sxs-lookup"><span data-stu-id="8e6ff-130">-Scope</span></span>
<span data-ttu-id="8e6ff-131">Zakres subskrypcji, czy to zakres api /apis/{apiId} lub zakres produktu /products/{productId}, zakres /apis lub zakres globalny /.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="8e6ff-132">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-132">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e6ff-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="8e6ff-133">-SecondaryKey</span></span>
<span data-ttu-id="8e6ff-134">Określa klucz pomocniczy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="8e6ff-135">Ten parametr jest generowany automatycznie, jeśli nie został określony.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="8e6ff-136">Ten parametr musi mieć od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="8e6ff-137">— województwo</span><span class="sxs-lookup"><span data-stu-id="8e6ff-137">-State</span></span>
<span data-ttu-id="8e6ff-138">Określa stan subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-138">Specifies the subscription state.</span></span>
<span data-ttu-id="8e6ff-139">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-139">The default value is $Null.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState]
Parameter Sets: (All)
Aliases:
Accepted values: Suspended, Active, Expired, Submitted, Rejected, Cancelled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e6ff-140">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8e6ff-140">-SubscriptionId</span></span>
<span data-ttu-id="8e6ff-141">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="8e6ff-142">Ten parametr jest generowany, jeśli nie został określony.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="8e6ff-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="8e6ff-143">-UserId</span></span>
<span data-ttu-id="8e6ff-144">Określa identyfikator subskrybenta.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-144">Specifies the subscriber ID.</span></span>

```yaml
Type: System.String
Parameter Sets: OldSubscriptionModel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NewSubscriptionModel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e6ff-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e6ff-145">CommonParameters</span></span>
<span data-ttu-id="8e6ff-146">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e6ff-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e6ff-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e6ff-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e6ff-148">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e6ff-148">INPUTS</span></span>

### <span data-ttu-id="8e6ff-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8e6ff-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8e6ff-150">System.String</span><span class="sxs-lookup"><span data-stu-id="8e6ff-150">System.String</span></span>

### <span data-ttu-id="8e6ff-151">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlet.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8e6ff-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8e6ff-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e6ff-152">OUTPUTS</span></span>

### <span data-ttu-id="8e6ff-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8e6ff-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="8e6ff-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8e6ff-154">NOTES</span></span>

## <span data-ttu-id="8e6ff-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e6ff-155">RELATED LINKS</span></span>

[<span data-ttu-id="8e6ff-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8e6ff-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="8e6ff-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8e6ff-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="8e6ff-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="8e6ff-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


