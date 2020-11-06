---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: a978fce4d44a061796597f2f3ae08c78c1021bdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547188"
---
# <span data-ttu-id="b403f-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b403f-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="b403f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b403f-102">SYNOPSIS</span></span>
<span data-ttu-id="b403f-103">Tworzy produkt zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b403f-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b403f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b403f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b403f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b403f-105">DESCRIPTION</span></span>
<span data-ttu-id="b403f-106">Polecenie cmdlet **New-AzureRmApiManagementProduct** umożliwia utworzenie produktu do zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b403f-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="b403f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b403f-107">EXAMPLES</span></span>

### <span data-ttu-id="b403f-108">Przykład 1. Tworzenie produktu, który nie wymaga subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b403f-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="b403f-109">To polecenie tworzy produkt zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b403f-109">This command creates an API Management product.</span></span>
<span data-ttu-id="b403f-110">Nie jest wymagana żadna subskrypcja.</span><span class="sxs-lookup"><span data-stu-id="b403f-110">No subscription is required.</span></span>

### <span data-ttu-id="b403f-111">Przykład 2: tworzenie produktu wymagającego abonamentu i zatwierdzenia</span><span class="sxs-lookup"><span data-stu-id="b403f-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="b403f-112">To polecenie tworzy produkt.</span><span class="sxs-lookup"><span data-stu-id="b403f-112">This command creates a product.</span></span>
<span data-ttu-id="b403f-113">Wymagany jest abonament i zatwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b403f-113">A subscription and approval are required.</span></span>
<span data-ttu-id="b403f-114">To polecenie ustawia okres powiadomienia na 10 dni.</span><span class="sxs-lookup"><span data-stu-id="b403f-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="b403f-115">Czas trwania abonamentu jest ustawiany na rok.</span><span class="sxs-lookup"><span data-stu-id="b403f-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="b403f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b403f-116">PARAMETERS</span></span>

### <span data-ttu-id="b403f-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="b403f-117">-ApprovalRequired</span></span>
<span data-ttu-id="b403f-118">Wskazuje, czy subskrypcja produktu wymaga zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="b403f-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="b403f-119">Domyślnie ten parametr jest **$false**.</span><span class="sxs-lookup"><span data-stu-id="b403f-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="b403f-120">-Context</span><span class="sxs-lookup"><span data-stu-id="b403f-120">-Context</span></span>
<span data-ttu-id="b403f-121">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="b403f-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b403f-122">— Opis</span><span class="sxs-lookup"><span data-stu-id="b403f-122">-Description</span></span>
<span data-ttu-id="b403f-123">Określa opis produktu.</span><span class="sxs-lookup"><span data-stu-id="b403f-123">Specifies the product description.</span></span>

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

### <span data-ttu-id="b403f-124">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="b403f-124">-LegalTerms</span></span>
<span data-ttu-id="b403f-125">Określa warunki prawne użytkowania produktu.</span><span class="sxs-lookup"><span data-stu-id="b403f-125">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="b403f-126">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b403f-126">-ProductId</span></span>
<span data-ttu-id="b403f-127">Określa identyfikator nowego produktu.</span><span class="sxs-lookup"><span data-stu-id="b403f-127">Specifies the identifier of new product.</span></span>
<span data-ttu-id="b403f-128">Jeśli nie podano tego parametru, generowany jest nowy produkt.</span><span class="sxs-lookup"><span data-stu-id="b403f-128">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="b403f-129">-State</span><span class="sxs-lookup"><span data-stu-id="b403f-129">-State</span></span>
<span data-ttu-id="b403f-130">Określa stan produktu.</span><span class="sxs-lookup"><span data-stu-id="b403f-130">Specifies the product state.</span></span>
<span data-ttu-id="b403f-131">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="b403f-131">psdx_paramvalues</span></span>

- <span data-ttu-id="b403f-132">NotPublished</span><span class="sxs-lookup"><span data-stu-id="b403f-132">NotPublished</span></span>
- <span data-ttu-id="b403f-133">Podawane</span><span class="sxs-lookup"><span data-stu-id="b403f-133">Published</span></span> 

<span data-ttu-id="b403f-134">Wartość domyślna to NotPublished.</span><span class="sxs-lookup"><span data-stu-id="b403f-134">The default value is NotPublished.</span></span>

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

### <span data-ttu-id="b403f-135">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="b403f-135">-SubscriptionRequired</span></span>
<span data-ttu-id="b403f-136">Wskazuje, czy produkt wymaga subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b403f-136">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="b403f-137">Wartość domyślna to **$true**.</span><span class="sxs-lookup"><span data-stu-id="b403f-137">The default value is **$True**.</span></span>

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

### <span data-ttu-id="b403f-138">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="b403f-138">-SubscriptionsLimit</span></span>
<span data-ttu-id="b403f-139">Określa maksymalną liczbę jednoczesnych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b403f-139">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="b403f-140">Wartością domyślną jest 1.</span><span class="sxs-lookup"><span data-stu-id="b403f-140">The default value is 1.</span></span>

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

### <span data-ttu-id="b403f-141">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="b403f-141">-Title</span></span>
<span data-ttu-id="b403f-142">Określa tytuł produktu.</span><span class="sxs-lookup"><span data-stu-id="b403f-142">Specifies the product title.</span></span>

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

### <span data-ttu-id="b403f-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b403f-143">-DefaultProfile</span></span>
<span data-ttu-id="b403f-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b403f-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b403f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b403f-145">CommonParameters</span></span>
<span data-ttu-id="b403f-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b403f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b403f-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b403f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b403f-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b403f-148">INPUTS</span></span>

## <span data-ttu-id="b403f-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b403f-149">OUTPUTS</span></span>

### <span data-ttu-id="b403f-150">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b403f-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="b403f-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b403f-151">NOTES</span></span>

## <span data-ttu-id="b403f-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b403f-152">RELATED LINKS</span></span>

[<span data-ttu-id="b403f-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b403f-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="b403f-154">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b403f-154">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="b403f-155">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b403f-155">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


