---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: ea68d17d482a73a528cfe450a84700e48bfdd9f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064352"
---
# <span data-ttu-id="dda96-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dda96-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="dda96-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dda96-102">SYNOPSIS</span></span>
<span data-ttu-id="dda96-103">Tworzy abonament.</span><span class="sxs-lookup"><span data-stu-id="dda96-103">Creates a subscription.</span></span>

## <span data-ttu-id="dda96-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dda96-104">SYNTAX</span></span>

### <span data-ttu-id="dda96-105">OldSubscriptionModel (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dda96-105">OldSubscriptionModel (Default)</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dda96-106">NewSubscriptionModel</span><span class="sxs-lookup"><span data-stu-id="dda96-106">NewSubscriptionModel</span></span>
```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 [-UserId <String>] -Scope <String> [-PrimaryKey <String>] [-SecondaryKey <String>] [-AllowTracing]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dda96-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dda96-107">DESCRIPTION</span></span>
<span data-ttu-id="dda96-108">Polecenie cmdlet **New-AzApiManagementSubscription** tworzy abonament.</span><span class="sxs-lookup"><span data-stu-id="dda96-108">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="dda96-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dda96-109">EXAMPLES</span></span>

### <span data-ttu-id="dda96-110">Przykład 1: subskrybowanie użytkownika do produktu</span><span class="sxs-lookup"><span data-stu-id="dda96-110">Example 1: Subscribe a user to a product</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="dda96-111">To polecenie umożliwia zasubskrybowanie istniejącego użytkownika produktu.</span><span class="sxs-lookup"><span data-stu-id="dda96-111">This command subscribes an existing user to a product.</span></span>

### <span data-ttu-id="dda96-112">Przykład 2: Tworzenie abonamentu dla całego zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="dda96-112">Example 2: Create a subscription for all Api Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/apis" -Name "GlobalApiScope"
```

### <span data-ttu-id="dda96-113">Przykład 3: Tworzenie abonamentu dla zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="dda96-113">Example 3: Create a subscription for Product Scope</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $context -Scope "/products/starter" -Name "UnlimitedProductSub"
```

## <span data-ttu-id="dda96-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dda96-114">PARAMETERS</span></span>

### <span data-ttu-id="dda96-115">-AllowTracing</span><span class="sxs-lookup"><span data-stu-id="dda96-115">-AllowTracing</span></span>
<span data-ttu-id="dda96-116">Flaga określająca, czy można włączyć śledzenie na poziomie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="dda96-116">Flag which determines whether Tracing can be enabled at the Subscription Level.</span></span> <span data-ttu-id="dda96-117">To jest parametr opcjonalny, a wartość domyślna to $null.</span><span class="sxs-lookup"><span data-stu-id="dda96-117">This is optional parameter and default is $null.</span></span>

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

### <span data-ttu-id="dda96-118">-Context</span><span class="sxs-lookup"><span data-stu-id="dda96-118">-Context</span></span>
<span data-ttu-id="dda96-119">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="dda96-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dda96-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dda96-120">-DefaultProfile</span></span>
<span data-ttu-id="dda96-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dda96-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dda96-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dda96-122">-Name</span></span>
<span data-ttu-id="dda96-123">Określa nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dda96-123">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="dda96-124">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="dda96-124">-PrimaryKey</span></span>
<span data-ttu-id="dda96-125">Określa klucz podstawowy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dda96-125">Specifies the subscription primary key.</span></span>
<span data-ttu-id="dda96-126">Jeśli ten parametr nie jest określony, klucz jest generowany automatycznie.</span><span class="sxs-lookup"><span data-stu-id="dda96-126">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="dda96-127">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="dda96-127">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="dda96-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="dda96-128">-ProductId</span></span>
<span data-ttu-id="dda96-129">Określa identyfikator produktu, który ma zostać abonamentem.</span><span class="sxs-lookup"><span data-stu-id="dda96-129">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="dda96-130">-Zakres</span><span class="sxs-lookup"><span data-stu-id="dda96-130">-Scope</span></span>
<span data-ttu-id="dda96-131">Zakres subskrypcji, niezależnie od tego, czy jest to zakres API/apis/{apiId}, czy zakres/products/{productId} lub globalny zakres interfejsu API/Apis czy globalny zakres/.</span><span class="sxs-lookup"><span data-stu-id="dda96-131">The Scope of the Subscription, whether it is Api Scope /apis/{apiId} or Product Scope /products/{productId} or Global API Scope /apis or Global scope /.</span></span> <span data-ttu-id="dda96-132">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dda96-132">This parameter is required.</span></span>

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

### <span data-ttu-id="dda96-133">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="dda96-133">-SecondaryKey</span></span>
<span data-ttu-id="dda96-134">Określa klucz pomocniczy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dda96-134">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="dda96-135">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="dda96-135">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="dda96-136">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="dda96-136">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="dda96-137">-State</span><span class="sxs-lookup"><span data-stu-id="dda96-137">-State</span></span>
<span data-ttu-id="dda96-138">Określa stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="dda96-138">Specifies the subscription state.</span></span>
<span data-ttu-id="dda96-139">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="dda96-139">The default value is $Null.</span></span>

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

### <span data-ttu-id="dda96-140">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dda96-140">-SubscriptionId</span></span>
<span data-ttu-id="dda96-141">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dda96-141">Specifies the subscription ID.</span></span>
<span data-ttu-id="dda96-142">Ten parametr jest generowany, jeśli nie określono.</span><span class="sxs-lookup"><span data-stu-id="dda96-142">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="dda96-143">-UserId</span><span class="sxs-lookup"><span data-stu-id="dda96-143">-UserId</span></span>
<span data-ttu-id="dda96-144">Określa identyfikator subskrybenta.</span><span class="sxs-lookup"><span data-stu-id="dda96-144">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="dda96-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dda96-145">CommonParameters</span></span>
<span data-ttu-id="dda96-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dda96-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dda96-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dda96-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dda96-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dda96-148">INPUTS</span></span>

### <span data-ttu-id="dda96-149">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dda96-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dda96-150">System. String</span><span class="sxs-lookup"><span data-stu-id="dda96-150">System.String</span></span>

### <span data-ttu-id="dda96-151">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dda96-151">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dda96-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dda96-152">OUTPUTS</span></span>

### <span data-ttu-id="dda96-153">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dda96-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="dda96-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dda96-154">NOTES</span></span>

## <span data-ttu-id="dda96-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dda96-155">RELATED LINKS</span></span>

[<span data-ttu-id="dda96-156">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dda96-156">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="dda96-157">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dda96-157">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="dda96-158">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="dda96-158">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


