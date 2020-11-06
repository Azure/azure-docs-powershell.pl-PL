---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 636a969f6aef013ee947afbb43d398871848818a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549464"
---
# <span data-ttu-id="0509c-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0509c-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="0509c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0509c-102">SYNOPSIS</span></span>
<span data-ttu-id="0509c-103">Tworzy produkt zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0509c-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0509c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0509c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0509c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0509c-105">DESCRIPTION</span></span>
<span data-ttu-id="0509c-106">Polecenie cmdlet **New-AzureRmApiManagementProduct** umożliwia utworzenie produktu do zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0509c-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="0509c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0509c-107">EXAMPLES</span></span>

### <span data-ttu-id="0509c-108">Przykład 1. Tworzenie produktu, który nie wymaga subskrypcji</span><span class="sxs-lookup"><span data-stu-id="0509c-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="0509c-109">To polecenie tworzy produkt zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0509c-109">This command creates an API Management product.</span></span>
<span data-ttu-id="0509c-110">Nie jest wymagana żadna subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="0509c-110">No subscription is required.</span></span>

### <span data-ttu-id="0509c-111">Przykład 2: tworzenie produktu wymagającego abonamentu i zatwierdzenia</span><span class="sxs-lookup"><span data-stu-id="0509c-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="0509c-112">To polecenie tworzy produkt.</span><span class="sxs-lookup"><span data-stu-id="0509c-112">This command creates a product.</span></span>
<span data-ttu-id="0509c-113">Wymagany jest abonament i zatwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0509c-113">A subscription and approval are required.</span></span>
<span data-ttu-id="0509c-114">To polecenie ustawia okres powiadomienia na 10 dni.</span><span class="sxs-lookup"><span data-stu-id="0509c-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="0509c-115">Czas trwania abonamentu jest ustawiany na rok.</span><span class="sxs-lookup"><span data-stu-id="0509c-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="0509c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0509c-116">PARAMETERS</span></span>

### <span data-ttu-id="0509c-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="0509c-117">-ApprovalRequired</span></span>
<span data-ttu-id="0509c-118">Wskazuje, czy subskrypcja produktu wymaga zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="0509c-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="0509c-119">Domyślnie ten parametr jest **$false**.</span><span class="sxs-lookup"><span data-stu-id="0509c-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="0509c-120">-Context</span><span class="sxs-lookup"><span data-stu-id="0509c-120">-Context</span></span>
<span data-ttu-id="0509c-121">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="0509c-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0509c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0509c-122">-DefaultProfile</span></span>
<span data-ttu-id="0509c-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0509c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0509c-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="0509c-124">-Description</span></span>
<span data-ttu-id="0509c-125">Określa opis produktu.</span><span class="sxs-lookup"><span data-stu-id="0509c-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="0509c-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="0509c-126">-LegalTerms</span></span>
<span data-ttu-id="0509c-127">Określa warunki prawne użytkowania produktu.</span><span class="sxs-lookup"><span data-stu-id="0509c-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="0509c-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="0509c-128">-ProductId</span></span>
<span data-ttu-id="0509c-129">Określa identyfikator nowego produktu.</span><span class="sxs-lookup"><span data-stu-id="0509c-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="0509c-130">Jeśli nie podano tego parametru, generowany jest nowy produkt.</span><span class="sxs-lookup"><span data-stu-id="0509c-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="0509c-131">-State</span><span class="sxs-lookup"><span data-stu-id="0509c-131">-State</span></span>
<span data-ttu-id="0509c-132">Określa stan produktu.</span><span class="sxs-lookup"><span data-stu-id="0509c-132">Specifies the product state.</span></span>
<span data-ttu-id="0509c-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="0509c-133">psdx_paramvalues</span></span>
- <span data-ttu-id="0509c-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="0509c-134">NotPublished</span></span>
- <span data-ttu-id="0509c-135">Opublikowano wartość domyślną to NotPublished.</span><span class="sxs-lookup"><span data-stu-id="0509c-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="0509c-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="0509c-136">-SubscriptionRequired</span></span>
<span data-ttu-id="0509c-137">Wskazuje, czy produkt wymaga subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0509c-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="0509c-138">Wartość domyślna to **$true**.</span><span class="sxs-lookup"><span data-stu-id="0509c-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="0509c-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="0509c-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="0509c-140">Określa maksymalną liczbę jednoczesnych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="0509c-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="0509c-141">Wartością domyślną jest 1.</span><span class="sxs-lookup"><span data-stu-id="0509c-141">The default value is 1.</span></span>

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

### <span data-ttu-id="0509c-142">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="0509c-142">-Title</span></span>
<span data-ttu-id="0509c-143">Określa tytuł produktu.</span><span class="sxs-lookup"><span data-stu-id="0509c-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="0509c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0509c-144">CommonParameters</span></span>
<span data-ttu-id="0509c-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0509c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0509c-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0509c-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0509c-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0509c-147">INPUTS</span></span>

### <span data-ttu-id="0509c-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0509c-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0509c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="0509c-149">System.String</span></span>

### <span data-ttu-id="0509c-150">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0509c-150">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0509c-151">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0509c-151">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0509c-152">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementProductState, Microsoft. Azure. Commands. ApiManagement. servicemanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="0509c-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0509c-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0509c-153">OUTPUTS</span></span>

### <span data-ttu-id="0509c-154">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0509c-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="0509c-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0509c-155">NOTES</span></span>

## <span data-ttu-id="0509c-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0509c-156">RELATED LINKS</span></span>

[<span data-ttu-id="0509c-157">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0509c-157">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="0509c-158">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0509c-158">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="0509c-159">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="0509c-159">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


