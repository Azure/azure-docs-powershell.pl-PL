---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 8695d8866b83ed6cd7b29a3d94546da1114d3eb5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550411"
---
# <span data-ttu-id="e6d0c-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e6d0c-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="e6d0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6d0c-102">SYNOPSIS</span></span>
<span data-ttu-id="e6d0c-103">Pobiera abonamenty.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6d0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6d0c-104">SYNTAX</span></span>

### <span data-ttu-id="e6d0c-105">GetAllSubscriptions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e6d0c-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6d0c-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e6d0c-106">GetBySubscriptionId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6d0c-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="e6d0c-107">GetByUserId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6d0c-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="e6d0c-108">GetByProductId</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6d0c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e6d0c-109">DESCRIPTION</span></span>
<span data-ttu-id="e6d0c-110">Polecenie cmdlet **Get-AzureRmApiManagementSubscription** pobiera określoną subskrypcję lub wszystkie subskrypcje, jeśli nie określono abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="e6d0c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6d0c-111">EXAMPLES</span></span>

### <span data-ttu-id="e6d0c-112">Przykład 1: Uzyskaj wszystkie subskrypcje</span><span class="sxs-lookup"><span data-stu-id="e6d0c-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="e6d0c-113">To polecenie pobiera wszystkie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="e6d0c-114">Przykład 2: uzyskiwanie abonamentu o określonym IDENTYFIKATORze</span><span class="sxs-lookup"><span data-stu-id="e6d0c-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="e6d0c-115">To polecenie pobiera abonament według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="e6d0c-116">Przykład 3: uzyskiwanie wszystkich subskrypcji dla użytkownika</span><span class="sxs-lookup"><span data-stu-id="e6d0c-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="e6d0c-117">To polecenie uzyskuje subskrypcje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="e6d0c-118">Przykład 4: uzyskiwanie wszystkich subskrypcji produktu</span><span class="sxs-lookup"><span data-stu-id="e6d0c-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="e6d0c-119">To polecenie pobiera wszystkie subskrypcje produktu.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="e6d0c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6d0c-120">PARAMETERS</span></span>

### <span data-ttu-id="e6d0c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="e6d0c-121">-Context</span></span>
<span data-ttu-id="e6d0c-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e6d0c-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e6d0c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6d0c-123">-DefaultProfile</span></span>
<span data-ttu-id="e6d0c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6d0c-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e6d0c-125">-ProductId</span></span>
<span data-ttu-id="e6d0c-126">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-126">Specifies a product identifier.</span></span>
<span data-ttu-id="e6d0c-127">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora produktu.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="e6d0c-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e6d0c-128">-SubscriptionId</span></span>
<span data-ttu-id="e6d0c-129">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="e6d0c-130">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie abonamentu o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="e6d0c-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="e6d0c-131">-UserId</span></span>
<span data-ttu-id="e6d0c-132">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-132">Specifies a user identifier.</span></span>
<span data-ttu-id="e6d0c-133">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="e6d0c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6d0c-134">CommonParameters</span></span>
<span data-ttu-id="e6d0c-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6d0c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6d0c-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6d0c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6d0c-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6d0c-137">INPUTS</span></span>

### <span data-ttu-id="e6d0c-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e6d0c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e6d0c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e6d0c-139">System.String</span></span>

## <span data-ttu-id="e6d0c-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6d0c-140">OUTPUTS</span></span>

### <span data-ttu-id="e6d0c-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e6d0c-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="e6d0c-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6d0c-142">NOTES</span></span>

## <span data-ttu-id="e6d0c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6d0c-143">RELATED LINKS</span></span>

[<span data-ttu-id="e6d0c-144">Nowe — AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e6d0c-144">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="e6d0c-145">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e6d0c-145">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="e6d0c-146">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="e6d0c-146">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


