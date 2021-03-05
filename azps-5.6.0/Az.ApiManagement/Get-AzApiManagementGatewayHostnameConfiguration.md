---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 27e833c526dea1b8df6451671ae2fd142c00b6e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981329"
---
# <span data-ttu-id="5b5d1-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b5d1-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="5b5d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b5d1-102">SYNOPSIS</span></span>
<span data-ttu-id="5b5d1-103">Pobiera całą konfigurację lub określoną nazwę hosta dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="5b5d1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b5d1-104">SYNTAX</span></span>

### <span data-ttu-id="5b5d1-105">GetByGatewayId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5b5d1-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b5d1-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="5b5d1-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b5d1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b5d1-107">DESCRIPTION</span></span>
<span data-ttu-id="5b5d1-108">Polecenie **cmdlet Get-AzApiManagementGatewayHostnameConfiguration** pobiera całą lub określoną konfigurację nazwy hosta dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="5b5d1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b5d1-109">EXAMPLES</span></span>

### <span data-ttu-id="5b5d1-110">Przykład 1. Uzyskiwanie wszystkich konfiguracji nazwy hosta dla bramy</span><span class="sxs-lookup"><span data-stu-id="5b5d1-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="5b5d1-111">To polecenie pobiera wszystkie konfiguracje nazw hostów dla bramy "0123456789".</span><span class="sxs-lookup"><span data-stu-id="5b5d1-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="5b5d1-112">Przykład 2. Uzyskiwanie konfiguracji nazwy hosta bramy</span><span class="sxs-lookup"><span data-stu-id="5b5d1-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="5b5d1-113">To polecenie pobiera konfigurację nazwy hosta "123" dla bramy "0123456789".</span><span class="sxs-lookup"><span data-stu-id="5b5d1-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="5b5d1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b5d1-114">PARAMETERS</span></span>

### <span data-ttu-id="5b5d1-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="5b5d1-115">-Context</span></span>
<span data-ttu-id="5b5d1-116">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5b5d1-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-117">This parameter is required.</span></span>

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

### <span data-ttu-id="5b5d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b5d1-118">-DefaultProfile</span></span>
<span data-ttu-id="5b5d1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b5d1-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5b5d1-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="5b5d1-121">Identyfikator konfiguracji nazwy hosta.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="5b5d1-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-122">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByGatewayHostnameId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b5d1-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="5b5d1-123">-GatewayId</span></span>
<span data-ttu-id="5b5d1-124">Identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-124">Gateway identifier.</span></span>
<span data-ttu-id="5b5d1-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-125">This parameter is required.</span></span>

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

### <span data-ttu-id="5b5d1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b5d1-126">CommonParameters</span></span>
<span data-ttu-id="5b5d1-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b5d1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b5d1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b5d1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b5d1-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b5d1-129">INPUTS</span></span>

### <span data-ttu-id="5b5d1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5b5d1-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5b5d1-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5b5d1-131">System.String</span></span>

## <span data-ttu-id="5b5d1-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b5d1-132">OUTPUTS</span></span>

### <span data-ttu-id="5b5d1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b5d1-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="5b5d1-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b5d1-134">NOTES</span></span>

## <span data-ttu-id="5b5d1-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b5d1-135">RELATED LINKS</span></span>
