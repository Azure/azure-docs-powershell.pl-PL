---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 80b059a82264cf7d0adedbfca477616abcaa232d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502497"
---
# <span data-ttu-id="37c5f-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="37c5f-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="37c5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="37c5f-103">Pobiera całą lub określoną bramę zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="37c5f-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="37c5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37c5f-104">SYNTAX</span></span>

### <span data-ttu-id="37c5f-105">GetAllGateways (domyślny)</span><span class="sxs-lookup"><span data-stu-id="37c5f-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="37c5f-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="37c5f-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37c5f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="37c5f-107">DESCRIPTION</span></span>
<span data-ttu-id="37c5f-108">Polecenie cmdlet **Get-AzApiManagementGateway** pobiera całą bramę zarządzania API lub określoną.</span><span class="sxs-lookup"><span data-stu-id="37c5f-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="37c5f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37c5f-109">EXAMPLES</span></span>

### <span data-ttu-id="37c5f-110">Przykład 1: Pobierz wszystkie bramy</span><span class="sxs-lookup"><span data-stu-id="37c5f-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="37c5f-111">To polecenie pobiera wszystkie bramy.</span><span class="sxs-lookup"><span data-stu-id="37c5f-111">This command gets all gateways.</span></span>

### <span data-ttu-id="37c5f-112">Przykład 2: uzyskiwanie bramy za pomocą identyfikatora</span><span class="sxs-lookup"><span data-stu-id="37c5f-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="37c5f-113">To polecenie pobiera bramkę 0123456789.</span><span class="sxs-lookup"><span data-stu-id="37c5f-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="37c5f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37c5f-114">PARAMETERS</span></span>

### <span data-ttu-id="37c5f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="37c5f-115">-Context</span></span>
<span data-ttu-id="37c5f-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="37c5f-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="37c5f-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="37c5f-117">This parameter is required.</span></span>

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

### <span data-ttu-id="37c5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37c5f-118">-DefaultProfile</span></span>
<span data-ttu-id="37c5f-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37c5f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37c5f-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="37c5f-120">-GatewayId</span></span>
<span data-ttu-id="37c5f-121">Identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="37c5f-121">Identifier of a gateway.</span></span>
<span data-ttu-id="37c5f-122">Jeśli zostanie określona, spróbuje znaleźć bramę za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="37c5f-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="37c5f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37c5f-123">CommonParameters</span></span>
<span data-ttu-id="37c5f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37c5f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37c5f-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37c5f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37c5f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37c5f-126">INPUTS</span></span>

### <span data-ttu-id="37c5f-127">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="37c5f-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="37c5f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="37c5f-128">System.String</span></span>

## <span data-ttu-id="37c5f-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37c5f-129">OUTPUTS</span></span>

### <span data-ttu-id="37c5f-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="37c5f-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="37c5f-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37c5f-131">NOTES</span></span>

## <span data-ttu-id="37c5f-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37c5f-132">RELATED LINKS</span></span>
