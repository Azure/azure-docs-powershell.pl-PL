---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178114"
---
# <span data-ttu-id="15aac-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="15aac-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="15aac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15aac-102">SYNOPSIS</span></span>
<span data-ttu-id="15aac-103">Otrzymuje klucze subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="15aac-103">Gets subscription keys.</span></span>

## <span data-ttu-id="15aac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="15aac-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15aac-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="15aac-105">DESCRIPTION</span></span>
<span data-ttu-id="15aac-106">Polecenie **cmdlet Get-AzApiManagementSubscriptionKey** otrzymuje klucze określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="15aac-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="15aac-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="15aac-107">EXAMPLES</span></span>

### <span data-ttu-id="15aac-108">Przykład 1. Uzyskiwanie kluczy subskrypcji o określonym identyfikatorze</span><span class="sxs-lookup"><span data-stu-id="15aac-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="15aac-109">To polecenie otrzymuje subskrypcję według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="15aac-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="15aac-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15aac-110">PARAMETERS</span></span>

### <span data-ttu-id="15aac-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="15aac-111">-Context</span></span>
<span data-ttu-id="15aac-112">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="15aac-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="15aac-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15aac-113">-DefaultProfile</span></span>
<span data-ttu-id="15aac-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="15aac-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15aac-115">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="15aac-115">-SubscriptionId</span></span>
<span data-ttu-id="15aac-116">Określa identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="15aac-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="15aac-117">Jeśli zostanie określone, to polecenie cmdlet znajdzie subskrypcję za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="15aac-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="15aac-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15aac-118">CommonParameters</span></span>
<span data-ttu-id="15aac-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15aac-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15aac-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15aac-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15aac-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15aac-121">INPUTS</span></span>

### <span data-ttu-id="15aac-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="15aac-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="15aac-123">System.String</span><span class="sxs-lookup"><span data-stu-id="15aac-123">System.String</span></span>

## <span data-ttu-id="15aac-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15aac-124">OUTPUTS</span></span>

### <span data-ttu-id="15aac-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="15aac-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="15aac-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="15aac-126">NOTES</span></span>

## <span data-ttu-id="15aac-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15aac-127">RELATED LINKS</span></span>

[<span data-ttu-id="15aac-128">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="15aac-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="15aac-129">New-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="15aac-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="15aac-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="15aac-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="15aac-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="15aac-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


