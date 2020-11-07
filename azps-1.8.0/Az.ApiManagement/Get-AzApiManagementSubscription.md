---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscription.md
ms.openlocfilehash: 885d552f6040d4c88c007a37f839ac030ba671c6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704633"
---
# <span data-ttu-id="58b9c-101">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="58b9c-101">Get-AzApiManagementSubscription</span></span>

## <span data-ttu-id="58b9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="58b9c-103">Pobiera abonamenty.</span><span class="sxs-lookup"><span data-stu-id="58b9c-103">Gets subscriptions.</span></span>

## <span data-ttu-id="58b9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58b9c-104">SYNTAX</span></span>

### <span data-ttu-id="58b9c-105">GetAllSubscriptions (domyślny)</span><span class="sxs-lookup"><span data-stu-id="58b9c-105">GetAllSubscriptions (Default)</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="58b9c-106">GetBySubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58b9c-106">GetBySubscriptionId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58b9c-107">GetByUserId</span><span class="sxs-lookup"><span data-stu-id="58b9c-107">GetByUserId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-UserId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58b9c-108">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="58b9c-108">GetByProductId</span></span>
```
Get-AzApiManagementSubscription -Context <PsApiManagementContext> [-ProductId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58b9c-109">Opis</span><span class="sxs-lookup"><span data-stu-id="58b9c-109">DESCRIPTION</span></span>
<span data-ttu-id="58b9c-110">Polecenie cmdlet **Get-AzApiManagementSubscription** pobiera określoną subskrypcję lub wszystkie subskrypcje, jeśli nie określono abonamentu.</span><span class="sxs-lookup"><span data-stu-id="58b9c-110">The **Get-AzApiManagementSubscription** cmdlet gets a specified subscription, or all subscriptions, if no subscription is specified.</span></span>

## <span data-ttu-id="58b9c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58b9c-111">EXAMPLES</span></span>

### <span data-ttu-id="58b9c-112">Przykład 1: Uzyskaj wszystkie subskrypcje</span><span class="sxs-lookup"><span data-stu-id="58b9c-112">Example 1: Get all subscriptions</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext
```

<span data-ttu-id="58b9c-113">To polecenie pobiera wszystkie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="58b9c-113">This command gets all subscriptions.</span></span>

### <span data-ttu-id="58b9c-114">Przykład 2: uzyskiwanie abonamentu o określonym IDENTYFIKATORze</span><span class="sxs-lookup"><span data-stu-id="58b9c-114">Example 2: Get a subscription with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -SubscriptionId "0123456789"
```

<span data-ttu-id="58b9c-115">To polecenie pobiera abonament według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="58b9c-115">This command gets a subscription by ID.</span></span>

### <span data-ttu-id="58b9c-116">Przykład 3: uzyskiwanie wszystkich subskrypcji dla użytkownika</span><span class="sxs-lookup"><span data-stu-id="58b9c-116">Example 3: Get all subscriptions for a user</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -UserId "777"
```

<span data-ttu-id="58b9c-117">To polecenie uzyskuje subskrypcje użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58b9c-117">This command gets a user's subscriptions.</span></span>

### <span data-ttu-id="58b9c-118">Przykład 4: uzyskiwanie wszystkich subskrypcji produktu</span><span class="sxs-lookup"><span data-stu-id="58b9c-118">Example 4: Get all subscriptions for a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscription -Context $apimContext -ProductId "999"
```

<span data-ttu-id="58b9c-119">To polecenie pobiera wszystkie subskrypcje produktu.</span><span class="sxs-lookup"><span data-stu-id="58b9c-119">This command gets all subscriptions for the product.</span></span>

## <span data-ttu-id="58b9c-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58b9c-120">PARAMETERS</span></span>

### <span data-ttu-id="58b9c-121">-Context</span><span class="sxs-lookup"><span data-stu-id="58b9c-121">-Context</span></span>
<span data-ttu-id="58b9c-122">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="58b9c-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="58b9c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58b9c-123">-DefaultProfile</span></span>
<span data-ttu-id="58b9c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="58b9c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58b9c-125">-ProductId</span><span class="sxs-lookup"><span data-stu-id="58b9c-125">-ProductId</span></span>
<span data-ttu-id="58b9c-126">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="58b9c-126">Specifies a product identifier.</span></span>
<span data-ttu-id="58b9c-127">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora produktu.</span><span class="sxs-lookup"><span data-stu-id="58b9c-127">If specified, this cmdlet finds all subscriptions by the product identifier.</span></span>

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

### <span data-ttu-id="58b9c-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="58b9c-128">-SubscriptionId</span></span>
<span data-ttu-id="58b9c-129">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="58b9c-129">Specifies a subscription identifier.</span></span>
<span data-ttu-id="58b9c-130">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie abonamentu o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="58b9c-130">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="58b9c-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="58b9c-131">-UserId</span></span>
<span data-ttu-id="58b9c-132">Określa identyfikator użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58b9c-132">Specifies a user identifier.</span></span>
<span data-ttu-id="58b9c-133">Jeśli ta funkcja jest określona, to polecenie cmdlet wyszukuje wszystkie subskrypcje według identyfikatora użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58b9c-133">If specified, this cmdlet finds all subscriptions by the user identifier.</span></span>

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

### <span data-ttu-id="58b9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58b9c-134">CommonParameters</span></span>
<span data-ttu-id="58b9c-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58b9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58b9c-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58b9c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58b9c-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58b9c-137">INPUTS</span></span>

### <span data-ttu-id="58b9c-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="58b9c-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="58b9c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="58b9c-139">System.String</span></span>

## <span data-ttu-id="58b9c-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58b9c-140">OUTPUTS</span></span>

### <span data-ttu-id="58b9c-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="58b9c-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="58b9c-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58b9c-142">NOTES</span></span>

## <span data-ttu-id="58b9c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58b9c-143">RELATED LINKS</span></span>

[<span data-ttu-id="58b9c-144">Nowe — AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="58b9c-144">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="58b9c-145">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="58b9c-145">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="58b9c-146">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="58b9c-146">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


