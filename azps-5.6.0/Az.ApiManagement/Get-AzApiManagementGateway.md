---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGateway.md
ms.openlocfilehash: 980adceb2e5a76532c9b3175c015d5f4e3a6b2e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999020"
---
# <span data-ttu-id="1b133-101">Get-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1b133-101">Get-AzApiManagementGateway</span></span>

## <span data-ttu-id="1b133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b133-102">SYNOPSIS</span></span>
<span data-ttu-id="1b133-103">Pobiera wszystkie lub określoną bramę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1b133-103">Gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="1b133-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1b133-104">SYNTAX</span></span>

### <span data-ttu-id="1b133-105">GetAllGateway (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1b133-105">GetAllGateways (Default)</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b133-106">GetByGatewayId</span><span class="sxs-lookup"><span data-stu-id="1b133-106">GetByGatewayId</span></span>
```
Get-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b133-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1b133-107">DESCRIPTION</span></span>
<span data-ttu-id="1b133-108">Polecenie **cmdlet Get-AzApiManagementGateway** pobiera wszystkie lub określone bramy zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="1b133-108">The **Get-AzApiManagementGateway** cmdlet gets all or specific API management Gateway.</span></span>

## <span data-ttu-id="1b133-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1b133-109">EXAMPLES</span></span>

### <span data-ttu-id="1b133-110">Przykład 1. Uzyskiwanie wszystkich bram</span><span class="sxs-lookup"><span data-stu-id="1b133-110">Example 1: Get all gateways</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext
```

<span data-ttu-id="1b133-111">To polecenie pobiera wszystkie bramy.</span><span class="sxs-lookup"><span data-stu-id="1b133-111">This command gets all gateways.</span></span>

### <span data-ttu-id="1b133-112">Przykład 2. Uzyskiwanie bramy według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="1b133-112">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGateway -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="1b133-113">To polecenie pobiera bramę 0123456789.</span><span class="sxs-lookup"><span data-stu-id="1b133-113">This command gets the gateway 0123456789.</span></span>

## <span data-ttu-id="1b133-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b133-114">PARAMETERS</span></span>

### <span data-ttu-id="1b133-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="1b133-115">-Context</span></span>
<span data-ttu-id="1b133-116">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1b133-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1b133-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1b133-117">This parameter is required.</span></span>

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

### <span data-ttu-id="1b133-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b133-118">-DefaultProfile</span></span>
<span data-ttu-id="1b133-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b133-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b133-120">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="1b133-120">-GatewayId</span></span>
<span data-ttu-id="1b133-121">Identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="1b133-121">Identifier of a gateway.</span></span>
<span data-ttu-id="1b133-122">Jeśli zostanie określona, spróbuje znaleźć bramę za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="1b133-122">If specified will try to find gateway by the identifier.</span></span>

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

### <span data-ttu-id="1b133-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b133-123">CommonParameters</span></span>
<span data-ttu-id="1b133-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b133-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b133-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b133-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b133-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b133-126">INPUTS</span></span>

### <span data-ttu-id="1b133-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1b133-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1b133-128">System.String</span><span class="sxs-lookup"><span data-stu-id="1b133-128">System.String</span></span>

## <span data-ttu-id="1b133-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b133-129">OUTPUTS</span></span>

### <span data-ttu-id="1b133-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="1b133-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="1b133-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1b133-131">NOTES</span></span>

## <span data-ttu-id="1b133-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b133-132">RELATED LINKS</span></span>
