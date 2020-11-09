---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: d58d33789f491098a62d7628ce6495ef2ba8870b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307657"
---
# <span data-ttu-id="2e2ab-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="2e2ab-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="2e2ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e2ab-102">SYNOPSIS</span></span>
<span data-ttu-id="2e2ab-103">Pobiera klucze istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="2e2ab-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="2e2ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e2ab-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e2ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2e2ab-105">DESCRIPTION</span></span>
<span data-ttu-id="2e2ab-106">Polecenie cmdlet **Get-AzApiManagementGatewayKey** pobiera klucze istniejącej bramy</span><span class="sxs-lookup"><span data-stu-id="2e2ab-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="2e2ab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e2ab-107">EXAMPLES</span></span>

### <span data-ttu-id="2e2ab-108">Przykład 2: uzyskiwanie bramy za pomocą identyfikatora</span><span class="sxs-lookup"><span data-stu-id="2e2ab-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="2e2ab-109">To polecenie pobiera klucze bramy "0123456789".</span><span class="sxs-lookup"><span data-stu-id="2e2ab-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="2e2ab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e2ab-110">PARAMETERS</span></span>

### <span data-ttu-id="2e2ab-111">-Context</span><span class="sxs-lookup"><span data-stu-id="2e2ab-111">-Context</span></span>
<span data-ttu-id="2e2ab-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2e2ab-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2e2ab-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2e2ab-113">This parameter is required.</span></span>

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

### <span data-ttu-id="2e2ab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e2ab-114">-DefaultProfile</span></span>
<span data-ttu-id="2e2ab-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e2ab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e2ab-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="2e2ab-116">-GatewayId</span></span>
<span data-ttu-id="2e2ab-117">Identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="2e2ab-117">Gateway identifier.</span></span>
<span data-ttu-id="2e2ab-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2e2ab-118">This parameter is required.</span></span>

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

### <span data-ttu-id="2e2ab-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e2ab-119">CommonParameters</span></span>
<span data-ttu-id="2e2ab-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e2ab-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e2ab-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e2ab-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e2ab-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e2ab-122">INPUTS</span></span>

### <span data-ttu-id="2e2ab-123">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e2ab-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2e2ab-124">System. String</span><span class="sxs-lookup"><span data-stu-id="2e2ab-124">System.String</span></span>

## <span data-ttu-id="2e2ab-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e2ab-125">OUTPUTS</span></span>

### <span data-ttu-id="2e2ab-126">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="2e2ab-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="2e2ab-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e2ab-127">NOTES</span></span>

## <span data-ttu-id="2e2ab-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e2ab-128">RELATED LINKS</span></span>
