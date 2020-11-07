---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSubscription.md
ms.openlocfilehash: b836fec6074767e4b97188b5bb75f38d22724eb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869495"
---
# <span data-ttu-id="ddea8-101">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ddea8-101">New-AzApiManagementSubscription</span></span>

## <span data-ttu-id="ddea8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ddea8-102">SYNOPSIS</span></span>
<span data-ttu-id="ddea8-103">Tworzy abonament.</span><span class="sxs-lookup"><span data-stu-id="ddea8-103">Creates a subscription.</span></span>

## <span data-ttu-id="ddea8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ddea8-104">SYNTAX</span></span>

```
New-AzApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>] -Name <String>
 -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ddea8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ddea8-105">DESCRIPTION</span></span>
<span data-ttu-id="ddea8-106">Polecenie cmdlet **New-AzApiManagementSubscription** tworzy abonament.</span><span class="sxs-lookup"><span data-stu-id="ddea8-106">The **New-AzApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="ddea8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ddea8-107">EXAMPLES</span></span>

### <span data-ttu-id="ddea8-108">Przykład 1: subskrybowanie użytkownika do produktu</span><span class="sxs-lookup"><span data-stu-id="ddea8-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="ddea8-109">To polecenie umożliwia zasubskrybowanie istniejącego użytkownika produktu.</span><span class="sxs-lookup"><span data-stu-id="ddea8-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="ddea8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ddea8-110">PARAMETERS</span></span>

### <span data-ttu-id="ddea8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ddea8-111">-Context</span></span>
<span data-ttu-id="ddea8-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ddea8-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ddea8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddea8-113">-DefaultProfile</span></span>
<span data-ttu-id="ddea8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ddea8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ddea8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ddea8-115">-Name</span></span>
<span data-ttu-id="ddea8-116">Określa nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ddea8-116">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="ddea8-117">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="ddea8-117">-PrimaryKey</span></span>
<span data-ttu-id="ddea8-118">Określa klucz podstawowy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ddea8-118">Specifies the subscription primary key.</span></span>
<span data-ttu-id="ddea8-119">Jeśli ten parametr nie jest określony, klucz jest generowany automatycznie.</span><span class="sxs-lookup"><span data-stu-id="ddea8-119">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="ddea8-120">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="ddea8-120">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="ddea8-121">-ProductId</span><span class="sxs-lookup"><span data-stu-id="ddea8-121">-ProductId</span></span>
<span data-ttu-id="ddea8-122">Określa identyfikator produktu, który ma zostać abonamentem.</span><span class="sxs-lookup"><span data-stu-id="ddea8-122">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="ddea8-123">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="ddea8-123">-SecondaryKey</span></span>
<span data-ttu-id="ddea8-124">Określa klucz pomocniczy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ddea8-124">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="ddea8-125">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="ddea8-125">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="ddea8-126">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="ddea8-126">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="ddea8-127">-State</span><span class="sxs-lookup"><span data-stu-id="ddea8-127">-State</span></span>
<span data-ttu-id="ddea8-128">Określa stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="ddea8-128">Specifies the subscription state.</span></span>
<span data-ttu-id="ddea8-129">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="ddea8-129">The default value is $Null.</span></span>

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

### <span data-ttu-id="ddea8-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ddea8-130">-SubscriptionId</span></span>
<span data-ttu-id="ddea8-131">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ddea8-131">Specifies the subscription ID.</span></span>
<span data-ttu-id="ddea8-132">Ten parametr jest generowany, jeśli nie określono.</span><span class="sxs-lookup"><span data-stu-id="ddea8-132">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="ddea8-133">-UserId</span><span class="sxs-lookup"><span data-stu-id="ddea8-133">-UserId</span></span>
<span data-ttu-id="ddea8-134">Określa identyfikator subskrybenta.</span><span class="sxs-lookup"><span data-stu-id="ddea8-134">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="ddea8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddea8-135">CommonParameters</span></span>
<span data-ttu-id="ddea8-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddea8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddea8-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ddea8-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddea8-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddea8-138">INPUTS</span></span>

### <span data-ttu-id="ddea8-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ddea8-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ddea8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ddea8-140">System.String</span></span>

### <span data-ttu-id="ddea8-141">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementSubscriptionState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ddea8-141">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ddea8-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ddea8-142">OUTPUTS</span></span>

### <span data-ttu-id="ddea8-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ddea8-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="ddea8-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ddea8-144">NOTES</span></span>

## <span data-ttu-id="ddea8-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddea8-145">RELATED LINKS</span></span>

[<span data-ttu-id="ddea8-146">Get-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ddea8-146">Get-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="ddea8-147">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ddea8-147">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="ddea8-148">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="ddea8-148">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


