---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 1f863ad8e85a89b0a0af9290649944426709bf31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525413"
---
# <span data-ttu-id="73d3e-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73d3e-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="73d3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73d3e-102">SYNOPSIS</span></span>
<span data-ttu-id="73d3e-103">Pobiera abonamenty.</span><span class="sxs-lookup"><span data-stu-id="73d3e-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73d3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73d3e-104">SYNTAX</span></span>

### <span data-ttu-id="73d3e-105">GetAllSubscriptions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73d3e-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73d3e-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73d3e-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73d3e-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="73d3e-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73d3e-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="73d3e-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73d3e-109">Opis</span><span class="sxs-lookup"><span data-stu-id="73d3e-109">DESCRIPTION</span></span>
<span data-ttu-id="73d3e-110">Polecenie cmdlet **Get-AzureRmApiManagementSubscription** pobiera określoną subskrypcję lub wszystkie subskrypcje, jeśli nie określono abonamentu.</span><span class="sxs-lookup"><span data-stu-id="73d3e-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="73d3e-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73d3e-111">EXAMPLES</span></span>

### <span data-ttu-id="73d3e-112">Przykład 1: Uzyskaj wszystkie subskrypcje</span><span class="sxs-lookup"><span data-stu-id="73d3e-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="73d3e-113">To polecenie pobiera wszystkie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="73d3e-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="73d3e-114">Przykład 2: uzyskiwanie abonamentu o określonym IDENTYFIKATORze</span><span class="sxs-lookup"><span data-stu-id="73d3e-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="73d3e-115">To polecenie pobiera abonament według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="73d3e-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="73d3e-116">Przykład 3: uzyskiwanie wszystkich subskrypcji dla użytkownika</span><span class="sxs-lookup"><span data-stu-id="73d3e-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="73d3e-117">To polecenie uzyskuje subskrypcje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="73d3e-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="73d3e-118">Przykład 4: uzyskiwanie wszystkich subskrypcji produktu</span><span class="sxs-lookup"><span data-stu-id="73d3e-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="73d3e-119">To polecenie pobiera wszystkie subskrypcje produktu.</span><span class="sxs-lookup"><span data-stu-id="73d3e-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="73d3e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73d3e-120">PARAMETERS</span></span>

### <span data-ttu-id="73d3e-121">-Context</span><span class="sxs-lookup"><span data-stu-id="73d3e-121">-Context</span></span>
<span data-ttu-id="73d3e-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="73d3e-122">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d3e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73d3e-123">-DefaultProfile</span></span>
<span data-ttu-id="73d3e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73d3e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73d3e-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="73d3e-125">-ProductId</span></span>
<span data-ttu-id="73d3e-126">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="73d3e-126">Specifies a product identifier.</span></span>
<span data-ttu-id="73d3e-127">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora produktu.</span><span class="sxs-lookup"><span data-stu-id="73d3e-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d3e-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="73d3e-128">-SubscriptionId</span></span>
<span data-ttu-id="73d3e-129">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="73d3e-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="73d3e-130">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie abonamentu o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="73d3e-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetBySubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d3e-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="73d3e-131">-UserId</span></span>
<span data-ttu-id="73d3e-132">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="73d3e-132">Specifies a user identifier.</span></span>
<span data-ttu-id="73d3e-133">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora użytkownika.</span><span class="sxs-lookup"><span data-stu-id="73d3e-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: String
Parameter Sets: GetByUserId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73d3e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73d3e-134">CommonParameters</span></span>
<span data-ttu-id="73d3e-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73d3e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73d3e-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73d3e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73d3e-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73d3e-137">INPUTS</span></span>

### <span data-ttu-id="73d3e-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="73d3e-138">None</span></span>
<span data-ttu-id="73d3e-139">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="73d3e-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="73d3e-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73d3e-140">OUTPUTS</span></span>

### <span data-ttu-id="73d3e-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73d3e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>
<span data-ttu-id="73d3e-142">Szczegóły subskrypcji w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="73d3e-142">The detail of the subscription in the API Management service.</span></span>

### <span data-ttu-id="73d3e-143">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="73d3e-143">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>
<span data-ttu-id="73d3e-144">Lista abonamentów w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="73d3e-144">The list of subscription in API Management service.</span></span>

## <span data-ttu-id="73d3e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73d3e-145">NOTES</span></span>

## <span data-ttu-id="73d3e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73d3e-146">RELATED LINKS</span></span>

[<span data-ttu-id="73d3e-147">Nowe — AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73d3e-147">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="73d3e-148">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73d3e-148">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="73d3e-149">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="73d3e-149">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


