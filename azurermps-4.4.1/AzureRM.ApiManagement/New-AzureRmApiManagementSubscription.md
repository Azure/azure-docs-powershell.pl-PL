---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B85BF332-503D-41CB-A3B7-221B85B9BE30
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementSubscription.md
ms.openlocfilehash: 360bf469f5496d837d12fb6cd4fa8dba9cefd724
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552452"
---
# <span data-ttu-id="d8258-101">New-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8258-101">New-AzureRmApiManagementSubscription</span></span>

## <span data-ttu-id="d8258-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8258-102">SYNOPSIS</span></span>
<span data-ttu-id="d8258-103">Tworzy abonament.</span><span class="sxs-lookup"><span data-stu-id="d8258-103">Creates a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8258-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8258-104">SYNTAX</span></span>

```
New-AzureRmApiManagementSubscription -Context <PsApiManagementContext> [-SubscriptionId <String>]
 -Name <String> -UserId <String> -ProductId <String> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-State <PsApiManagementSubscriptionState>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8258-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8258-105">DESCRIPTION</span></span>
<span data-ttu-id="d8258-106">Polecenie cmdlet **New-AzureRmApiManagementSubscription** tworzy abonament.</span><span class="sxs-lookup"><span data-stu-id="d8258-106">The **New-AzureRmApiManagementSubscription** cmdlet creates a subscription.</span></span>

## <span data-ttu-id="d8258-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8258-107">EXAMPLES</span></span>

### <span data-ttu-id="d8258-108">Przykład 1: subskrybowanie użytkownika do produktu</span><span class="sxs-lookup"><span data-stu-id="d8258-108">Example 1: Subscribe a user to a product</span></span>
```
PS C:\>New-AzureRmApiManagementSubscription -Context $apimContext -UserId "777" -ProductId "999"
```

<span data-ttu-id="d8258-109">To polecenie umożliwia zasubskrybowanie istniejącego użytkownika produktu.</span><span class="sxs-lookup"><span data-stu-id="d8258-109">This command subscribes an existing user to a product.</span></span>

## <span data-ttu-id="d8258-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8258-110">PARAMETERS</span></span>

### <span data-ttu-id="d8258-111">-Context</span><span class="sxs-lookup"><span data-stu-id="d8258-111">-Context</span></span>
<span data-ttu-id="d8258-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="d8258-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d8258-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8258-113">-Name</span></span>
<span data-ttu-id="d8258-114">Określa nazwę subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d8258-114">Specifies the subscription name.</span></span>

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

### <span data-ttu-id="d8258-115">-Primarykea</span><span class="sxs-lookup"><span data-stu-id="d8258-115">-PrimaryKey</span></span>
<span data-ttu-id="d8258-116">Określa klucz podstawowy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d8258-116">Specifies the subscription primary key.</span></span>
<span data-ttu-id="d8258-117">Jeśli ten parametr nie jest określony, klucz jest generowany automatycznie.</span><span class="sxs-lookup"><span data-stu-id="d8258-117">If this parameter is not specified the key is generated automatically.</span></span>
<span data-ttu-id="d8258-118">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="d8258-118">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="d8258-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="d8258-119">-ProductId</span></span>
<span data-ttu-id="d8258-120">Określa identyfikator produktu, który ma zostać abonamentem.</span><span class="sxs-lookup"><span data-stu-id="d8258-120">Specifies the ID of the product to which to subscribe.</span></span>

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

### <span data-ttu-id="d8258-121">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="d8258-121">-SecondaryKey</span></span>
<span data-ttu-id="d8258-122">Określa klucz pomocniczy subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d8258-122">Specifies the subscription secondary key.</span></span>
<span data-ttu-id="d8258-123">Ten parametr jest generowany automatycznie, jeśli nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="d8258-123">This parameter is generated automatically if it is not specified.</span></span>
<span data-ttu-id="d8258-124">Ten parametr musi mieć długość od 1 do 300 znaków.</span><span class="sxs-lookup"><span data-stu-id="d8258-124">This parameter must be 1 to 300 characters long.</span></span>

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

### <span data-ttu-id="d8258-125">-State</span><span class="sxs-lookup"><span data-stu-id="d8258-125">-State</span></span>
<span data-ttu-id="d8258-126">Określa stan abonamentu.</span><span class="sxs-lookup"><span data-stu-id="d8258-126">Specifies the subscription state.</span></span>
<span data-ttu-id="d8258-127">Wartość domyślna to $Null.</span><span class="sxs-lookup"><span data-stu-id="d8258-127">The default value is $Null.</span></span>

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

### <span data-ttu-id="d8258-128">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d8258-128">-SubscriptionId</span></span>
<span data-ttu-id="d8258-129">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d8258-129">Specifies the subscription ID.</span></span>
<span data-ttu-id="d8258-130">Ten parametr jest generowany, jeśli nie określono.</span><span class="sxs-lookup"><span data-stu-id="d8258-130">This parameter is generated if not specified.</span></span>

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

### <span data-ttu-id="d8258-131">-UserId</span><span class="sxs-lookup"><span data-stu-id="d8258-131">-UserId</span></span>
<span data-ttu-id="d8258-132">Określa identyfikator subskrybenta.</span><span class="sxs-lookup"><span data-stu-id="d8258-132">Specifies the subscriber ID.</span></span>

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

### <span data-ttu-id="d8258-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8258-133">-DefaultProfile</span></span>
<span data-ttu-id="d8258-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8258-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8258-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8258-135">CommonParameters</span></span>
<span data-ttu-id="d8258-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8258-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8258-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8258-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8258-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8258-138">INPUTS</span></span>

## <span data-ttu-id="d8258-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8258-139">OUTPUTS</span></span>

### <span data-ttu-id="d8258-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8258-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscription</span></span>

## <span data-ttu-id="d8258-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8258-141">NOTES</span></span>

## <span data-ttu-id="d8258-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8258-142">RELATED LINKS</span></span>

[<span data-ttu-id="d8258-143">Get-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8258-143">Get-AzureRmApiManagementSubscription</span></span>](./Get-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d8258-144">Remove-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8258-144">Remove-AzureRmApiManagementSubscription</span></span>](./Remove-AzureRmApiManagementSubscription.md)

[<span data-ttu-id="d8258-145">Set-AzureRmApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="d8258-145">Set-AzureRmApiManagementSubscription</span></span>](./Set-AzureRmApiManagementSubscription.md)


