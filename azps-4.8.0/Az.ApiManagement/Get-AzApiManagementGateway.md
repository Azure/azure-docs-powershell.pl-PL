---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223609"
---
# <span data-ttu-id="89d6c-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="89d6c-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="89d6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89d6c-102">SYNOPSIS</span></span>
<span data-ttu-id="89d6c-103">Pobiera całą lub określoną bramę zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="89d6c-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="89d6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89d6c-104">SYNTAX</span></span>

### <span data-ttu-id="89d6c-105">GetAllGateways (domyślny)</span><span class="sxs-lookup"><span data-stu-id="89d6c-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="89d6c-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="89d6c-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89d6c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="89d6c-107">DESCRIPTION</span></span>
<span data-ttu-id="89d6c-108">Polecenie cmdlet **Get-AzApiManagementGateway** pobiera całą bramę zarządzania API lub określoną.</span><span class="sxs-lookup"><span data-stu-id="89d6c-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="89d6c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89d6c-109">EXAMPLES</span></span>

### <span data-ttu-id="89d6c-110">Przykład 1: Pobierz wszystkie bramy</span><span class="sxs-lookup"><span data-stu-id="89d6c-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="89d6c-111">To polecenie pobiera wszystkie bramy.</span><span class="sxs-lookup"><span data-stu-id="89d6c-111">This command gets all gateways.</span></span>

### <span data-ttu-id="89d6c-112">Przykład 2: uzyskiwanie bramy za pomocą identyfikatora</span><span class="sxs-lookup"><span data-stu-id="89d6c-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="89d6c-113">To polecenie pobiera bramkę 0123456789.</span><span class="sxs-lookup"><span data-stu-id="89d6c-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="89d6c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89d6c-114">PARAMETERS</span></span>

### <span data-ttu-id="89d6c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="89d6c-115">-Context</span></span>
<span data-ttu-id="89d6c-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="89d6c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="89d6c-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="89d6c-117">This parameter is required.</span></span>

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

### <span data-ttu-id="89d6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d6c-118">-DefaultProfile</span></span>
<span data-ttu-id="89d6c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="89d6c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89d6c-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="89d6c-120">-GatewayId</span></span>
<span data-ttu-id="89d6c-121">Identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="89d6c-121">Identifier of a gateway.</span></span>
<span data-ttu-id="89d6c-122">Jeśli zostanie określona, spróbuje znaleźć bramę za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="89d6c-122">If specified will try to find gateway by the identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d6c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d6c-123">CommonParameters</span></span>
<span data-ttu-id="89d6c-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89d6c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d6c-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89d6c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d6c-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89d6c-126">INPUTS</span></span>

### <span data-ttu-id="89d6c-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="89d6c-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="89d6c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="89d6c-128">System.String</span></span>

## <span data-ttu-id="89d6c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89d6c-129">OUTPUTS</span></span>

### <span data-ttu-id="89d6c-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="89d6c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="89d6c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89d6c-131">NOTES</span></span>

## <span data-ttu-id="89d6c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89d6c-132">RELATED LINKS</span></span>
