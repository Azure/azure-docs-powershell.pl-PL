---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 173a8a7ab41b044d2a9442a9345ec59ab80329ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552479"
---
# <span data-ttu-id="2a4ce-101">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a4ce-101">Get-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="2a4ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a4ce-102">SYNOPSIS</span></span>
<span data-ttu-id="2a4ce-103">Pobiera abonamenty.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-103">Gets subscriptions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a4ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a4ce-104">SYNTAX</span></span>

### <span data-ttu-id="2a4ce-105">Pobieranie wszystkich subskrypcji (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2a4ce-105">Get all subscriptions (Default)</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a4ce-106">Uzyskaj według identyfikatora subsctiption</span><span class="sxs-lookup"><span data-stu-id="2a4ce-106">Get by subsctiption ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a4ce-107">Uzyskaj według identyfikatora użytkownika</span><span class="sxs-lookup"><span data-stu-id="2a4ce-107">Get by user ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a4ce-108">Pobierz według identyfikatora produktu</span><span class="sxs-lookup"><span data-stu-id="2a4ce-108">Get by product ID</span></span>
```
Get-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a4ce-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2a4ce-109">DESCRIPTION</span></span>
<span data-ttu-id="2a4ce-110">Polecenie cmdlet **Get-AzureRmApiManagementSubscription** pobiera określoną subskrypcję lub wszystkie subskrypcje, jeśli nie określono abonamentu.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-110">The **Get-AzureRmApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="2a4ce-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a4ce-111">EXAMPLES</span></span>

### <span data-ttu-id="2a4ce-112">Przykład 1: Uzyskaj wszystkie subskrypcje</span><span class="sxs-lookup"><span data-stu-id="2a4ce-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="2a4ce-113">To polecenie pobiera wszystkie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="2a4ce-114">Przykład 2: uzyskiwanie abonamentu o określonym IDENTYFIKATORze</span><span class="sxs-lookup"><span data-stu-id="2a4ce-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="2a4ce-115">To polecenie pobiera abonament według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="2a4ce-116">Przykład 3: uzyskiwanie wszystkich subskrypcji dla użytkownika</span><span class="sxs-lookup"><span data-stu-id="2a4ce-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="2a4ce-117">To polecenie uzyskuje subskrypcje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="2a4ce-118">Przykład 4: uzyskiwanie wszystkich subskrypcji produktu</span><span class="sxs-lookup"><span data-stu-id="2a4ce-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>Get-AzureRmApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="2a4ce-119">To polecenie pobiera wszystkie subskrypcje produktu.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="2a4ce-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a4ce-120">PARAMETERS</span></span>

### <span data-ttu-id="2a4ce-121">-Context</span><span class="sxs-lookup"><span data-stu-id="2a4ce-121">-Context</span></span>
<span data-ttu-id="2a4ce-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2a4ce-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2a4ce-123">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2a4ce-123">-ProductId</span></span>
<span data-ttu-id="2a4ce-124">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-124">Specifies a product identifier.</span></span>
<span data-ttu-id="2a4ce-125">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora produktu.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-125">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by product ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4ce-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2a4ce-126">-SubscriptionId</span></span>
<span data-ttu-id="2a4ce-127">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-127">Specifies a subscription identifier.</span></span>
<span data-ttu-id="2a4ce-128">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie abonamentu o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-128">If specified, this cmdlet finds subscription by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by subsctiption ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4ce-129">-UserId</span><span class="sxs-lookup"><span data-stu-id="2a4ce-129">-UserId</span></span>
<span data-ttu-id="2a4ce-130">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-130">Specifies a user identifier.</span></span>
<span data-ttu-id="2a4ce-131">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-131">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by user ID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a4ce-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a4ce-132">-DefaultProfile</span></span>
<span data-ttu-id="2a4ce-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a4ce-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a4ce-134">CommonParameters</span></span>
<span data-ttu-id="2a4ce-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a4ce-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a4ce-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a4ce-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a4ce-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a4ce-137">INPUTS</span></span>

## <span data-ttu-id="2a4ce-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a4ce-138">OUTPUTS</span></span>

### <span data-ttu-id="2a4ce-139">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementSubscription></span><span class="sxs-lookup"><span data-stu-id="2a4ce-139">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription></span></span>

## <span data-ttu-id="2a4ce-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a4ce-140">NOTES</span></span>

## <span data-ttu-id="2a4ce-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a4ce-141">RELATED LINKS</span></span>

[<span data-ttu-id="2a4ce-142">Nowe — AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a4ce-142">New-AzureRmApiManagementSubscription</span></span>](./New-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="2a4ce-143">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a4ce-143">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="2a4ce-144">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="2a4ce-144">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


