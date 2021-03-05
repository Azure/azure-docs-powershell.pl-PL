---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewaykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayKey.md
ms.openlocfilehash: 08931af2c5d4f4747bd02a759e374d8fccd247c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981322"
---
# <span data-ttu-id="bdd56-101">Get-AzApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="bdd56-101">Get-AzApiManagementGatewayKey</span></span>

## <span data-ttu-id="bdd56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdd56-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd56-103">Pobiera klucze istniejącej bramy</span><span class="sxs-lookup"><span data-stu-id="bdd56-103">Gets keys of the existing Gateway</span></span>

## <span data-ttu-id="bdd56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bdd56-104">SYNTAX</span></span>

```
Get-AzApiManagementGatewayKey -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bdd56-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bdd56-105">DESCRIPTION</span></span>
<span data-ttu-id="bdd56-106">Polecenie **cmdlet Get-AzApiManagementGatewayKey** pobiera klucze istniejącej bramy</span><span class="sxs-lookup"><span data-stu-id="bdd56-106">The **Get-AzApiManagementGatewayKey** cmdlet gets keys of the existing Gateway</span></span>

## <span data-ttu-id="bdd56-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bdd56-107">EXAMPLES</span></span>

### <span data-ttu-id="bdd56-108">Przykład 2. Uzyskiwanie bramy według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="bdd56-108">Example 2: Get a gateway by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayKey -Context $apimContext -GatewayId "0123456789"
```

<span data-ttu-id="bdd56-109">To polecenie pobiera klucze dla bramy "0123456789".</span><span class="sxs-lookup"><span data-stu-id="bdd56-109">This command gets the keys for a "0123456789" gateway.</span></span>

## <span data-ttu-id="bdd56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bdd56-110">PARAMETERS</span></span>

### <span data-ttu-id="bdd56-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="bdd56-111">-Context</span></span>
<span data-ttu-id="bdd56-112">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bdd56-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bdd56-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="bdd56-113">This parameter is required.</span></span>

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

### <span data-ttu-id="bdd56-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd56-114">-DefaultProfile</span></span>
<span data-ttu-id="bdd56-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd56-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdd56-116">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="bdd56-116">-GatewayId</span></span>
<span data-ttu-id="bdd56-117">Identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="bdd56-117">Gateway identifier.</span></span>
<span data-ttu-id="bdd56-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="bdd56-118">This parameter is required.</span></span>

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

### <span data-ttu-id="bdd56-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd56-119">CommonParameters</span></span>
<span data-ttu-id="bdd56-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd56-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd56-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bdd56-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd56-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdd56-122">INPUTS</span></span>

### <span data-ttu-id="bdd56-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bdd56-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bdd56-124">System.String</span><span class="sxs-lookup"><span data-stu-id="bdd56-124">System.String</span></span>

## <span data-ttu-id="bdd56-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdd56-125">OUTPUTS</span></span>

### <span data-ttu-id="bdd56-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span><span class="sxs-lookup"><span data-stu-id="bdd56-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayKey</span></span>

## <span data-ttu-id="bdd56-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bdd56-127">NOTES</span></span>

## <span data-ttu-id="bdd56-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdd56-128">RELATED LINKS</span></span>
