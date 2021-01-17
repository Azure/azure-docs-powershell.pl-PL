---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 3d14ef7dca35796baa3e3aecf0c3df98674bfb9b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382431"
---
# <span data-ttu-id="5b275-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5b275-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="5b275-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b275-102">SYNOPSIS</span></span>
<span data-ttu-id="5b275-103">Tworzy produkt zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="5b275-103">Creates an API Management product.</span></span>

## <span data-ttu-id="5b275-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b275-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b275-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5b275-105">DESCRIPTION</span></span>
<span data-ttu-id="5b275-106">Polecenie cmdlet **New-AzApiManagementProduct** umożliwia utworzenie produktu do zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="5b275-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="5b275-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b275-107">EXAMPLES</span></span>

### <span data-ttu-id="5b275-108">Przykład 1. Tworzenie produktu, który nie wymaga subskrypcji</span><span class="sxs-lookup"><span data-stu-id="5b275-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="5b275-109">To polecenie tworzy produkt zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="5b275-109">This command creates an API Management product.</span></span>
<span data-ttu-id="5b275-110">Nie jest wymagana żadna subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="5b275-110">No subscription is required.</span></span>

### <span data-ttu-id="5b275-111">Przykład 2: tworzenie produktu wymagającego abonamentu i zatwierdzenia</span><span class="sxs-lookup"><span data-stu-id="5b275-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="5b275-112">To polecenie tworzy produkt.</span><span class="sxs-lookup"><span data-stu-id="5b275-112">This command creates a product.</span></span>
<span data-ttu-id="5b275-113">Wymagany jest abonament i zatwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5b275-113">A subscription and approval are required.</span></span>
<span data-ttu-id="5b275-114">To polecenie ustawia okres powiadomienia na 10 dni.</span><span class="sxs-lookup"><span data-stu-id="5b275-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="5b275-115">Czas trwania abonamentu jest ustawiany na rok.</span><span class="sxs-lookup"><span data-stu-id="5b275-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="5b275-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b275-116">PARAMETERS</span></span>

### <span data-ttu-id="5b275-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="5b275-117">-ApprovalRequired</span></span>
<span data-ttu-id="5b275-118">Wskazuje, czy subskrypcja produktu wymaga zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="5b275-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="5b275-119">Domyślnie ten parametr jest **$false**.</span><span class="sxs-lookup"><span data-stu-id="5b275-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b275-120">-Context</span><span class="sxs-lookup"><span data-stu-id="5b275-120">-Context</span></span>
<span data-ttu-id="5b275-121">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5b275-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5b275-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b275-122">-DefaultProfile</span></span>
<span data-ttu-id="5b275-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b275-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b275-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="5b275-124">-Description</span></span>
<span data-ttu-id="5b275-125">Określa opis produktu.</span><span class="sxs-lookup"><span data-stu-id="5b275-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="5b275-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="5b275-126">-LegalTerms</span></span>
<span data-ttu-id="5b275-127">Określa warunki prawne użytkowania produktu.</span><span class="sxs-lookup"><span data-stu-id="5b275-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="5b275-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5b275-128">-ProductId</span></span>
<span data-ttu-id="5b275-129">Określa identyfikator nowego produktu.</span><span class="sxs-lookup"><span data-stu-id="5b275-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="5b275-130">Jeśli nie podano tego parametru, generowany jest nowy produkt.</span><span class="sxs-lookup"><span data-stu-id="5b275-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="5b275-131">-State</span><span class="sxs-lookup"><span data-stu-id="5b275-131">-State</span></span>
<span data-ttu-id="5b275-132">Określa stan produktu.</span><span class="sxs-lookup"><span data-stu-id="5b275-132">Specifies the product state.</span></span>
<span data-ttu-id="5b275-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="5b275-133">psdx_paramvalues</span></span>
- <span data-ttu-id="5b275-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="5b275-134">NotPublished</span></span>
- <span data-ttu-id="5b275-135">Opublikowano wartość domyślną to NotPublished.</span><span class="sxs-lookup"><span data-stu-id="5b275-135">Published The default value is NotPublished.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases:
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b275-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="5b275-136">-SubscriptionRequired</span></span>
<span data-ttu-id="5b275-137">Wskazuje, czy produkt wymaga subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5b275-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="5b275-138">Wartość domyślna to **$true**.</span><span class="sxs-lookup"><span data-stu-id="5b275-138">The default value is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b275-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="5b275-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="5b275-140">Określa maksymalną liczbę jednoczesnych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="5b275-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="5b275-141">Wartość domyślna to None.</span><span class="sxs-lookup"><span data-stu-id="5b275-141">The default value is None.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b275-142">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="5b275-142">-Title</span></span>
<span data-ttu-id="5b275-143">Określa tytuł produktu.</span><span class="sxs-lookup"><span data-stu-id="5b275-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="5b275-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b275-144">CommonParameters</span></span>
<span data-ttu-id="5b275-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b275-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b275-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b275-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b275-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b275-147">INPUTS</span></span>

### <span data-ttu-id="5b275-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5b275-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5b275-149">System. String</span><span class="sxs-lookup"><span data-stu-id="5b275-149">System.String</span></span>

### <span data-ttu-id="5b275-150">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5b275-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5b275-151">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5b275-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5b275-152">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementProductState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5b275-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5b275-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b275-153">OUTPUTS</span></span>

### <span data-ttu-id="5b275-154">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5b275-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="5b275-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b275-155">NOTES</span></span>

## <span data-ttu-id="5b275-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b275-156">RELATED LINKS</span></span>

[<span data-ttu-id="5b275-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5b275-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="5b275-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5b275-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="5b275-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="5b275-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


