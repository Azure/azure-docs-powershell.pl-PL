---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063030"
---
# <span data-ttu-id="6ade7-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="6ade7-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="6ade7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ade7-102">SYNOPSIS</span></span>
<span data-ttu-id="6ade7-103">Pobiera klucze subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6ade7-103">Gets subscription keys.</span></span>

## <span data-ttu-id="6ade7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ade7-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ade7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6ade7-105">DESCRIPTION</span></span>
<span data-ttu-id="6ade7-106">Polecenie cmdlet **Get-AzApiManagementSubscriptionKey** pobiera klucze określonego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="6ade7-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="6ade7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ade7-107">EXAMPLES</span></span>

### <span data-ttu-id="6ade7-108">Przykład 1: pobieranie kluczy subskrypcji z określonym IDENTYFIKATORem</span><span class="sxs-lookup"><span data-stu-id="6ade7-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="6ade7-109">To polecenie pobiera abonament według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="6ade7-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="6ade7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ade7-110">PARAMETERS</span></span>

### <span data-ttu-id="6ade7-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6ade7-111">-Context</span></span>
<span data-ttu-id="6ade7-112">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6ade7-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6ade7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ade7-113">-DefaultProfile</span></span>
<span data-ttu-id="6ade7-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ade7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ade7-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6ade7-115">-SubscriptionId</span></span>
<span data-ttu-id="6ade7-116">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6ade7-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="6ade7-117">Jeśli ta funkcja jest określona, to polecenie cmdlet umożliwia znalezienie abonamentu o identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="6ade7-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="6ade7-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ade7-118">CommonParameters</span></span>
<span data-ttu-id="6ade7-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ade7-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ade7-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ade7-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ade7-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ade7-121">INPUTS</span></span>

### <span data-ttu-id="6ade7-122">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6ade7-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6ade7-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6ade7-123">System.String</span></span>

## <span data-ttu-id="6ade7-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ade7-124">OUTPUTS</span></span>

### <span data-ttu-id="6ade7-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="6ade7-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="6ade7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ade7-126">NOTES</span></span>

## <span data-ttu-id="6ade7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ade7-127">RELATED LINKS</span></span>

[<span data-ttu-id="6ade7-128">Nowe — AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6ade7-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="6ade7-129">Nowe — AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6ade7-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="6ade7-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6ade7-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="6ade7-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="6ade7-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


