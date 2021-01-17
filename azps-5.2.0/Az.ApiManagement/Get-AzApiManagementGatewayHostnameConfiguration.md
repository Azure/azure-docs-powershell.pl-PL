---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ecdae500b0c1d81635e23ca6ca4bc4c803665912
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365444"
---
# <span data-ttu-id="f457c-101">Get-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f457c-101">Get-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="f457c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f457c-102">SYNOPSIS</span></span>
<span data-ttu-id="f457c-103">Pobiera wszystkie lub określoną konfigurację hosta dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="f457c-103">Gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="f457c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f457c-104">SYNTAX</span></span>

### <span data-ttu-id="f457c-105">GetByGatewayId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f457c-105">GetByGatewayId (Default)</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f457c-106">GetByGatewayHostnameId</span><span class="sxs-lookup"><span data-stu-id="f457c-106">GetByGatewayHostnameId</span></span>
```
Get-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f457c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f457c-107">DESCRIPTION</span></span>
<span data-ttu-id="f457c-108">Polecenie cmdlet **Get-AzApiManagementGatewayHostnameConfiguration** pobiera całą lub określoną konfigurację hosta dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="f457c-108">The **Get-AzApiManagementGatewayHostnameConfiguration** cmdlet gets all or specific hostname configuration for the existing Gateway.</span></span>

## <span data-ttu-id="f457c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f457c-109">EXAMPLES</span></span>

### <span data-ttu-id="f457c-110">Przykład 1: uzyskiwanie wszystkich konfiguracji hostów dla bramy</span><span class="sxs-lookup"><span data-stu-id="f457c-110">Example 1: Get all hostname configurations for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext  -GatewayId "0123456789"
```

<span data-ttu-id="f457c-111">To polecenie pobiera wszystkie konfiguracje nazw hostów dla bramy "0123456789".</span><span class="sxs-lookup"><span data-stu-id="f457c-111">This command gets all hostname configurations for a "0123456789" gateway.</span></span>

### <span data-ttu-id="f457c-112">Przykład 2: Uzyskiwanie konfiguracji nazwy hosta dla bramy</span><span class="sxs-lookup"><span data-stu-id="f457c-112">Example 2: Get a hostname configuration for the gateway</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "0123456789" -GatewayHostnameConfigurationId "123"
```

<span data-ttu-id="f457c-113">To polecenie pobiera konfigurację hosta "123" dla bramy "0123456789".</span><span class="sxs-lookup"><span data-stu-id="f457c-113">This command gets "123" hostname configuration for a "0123456789" gateway.</span></span>

## <span data-ttu-id="f457c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f457c-114">PARAMETERS</span></span>

### <span data-ttu-id="f457c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f457c-115">-Context</span></span>
<span data-ttu-id="f457c-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f457c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f457c-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f457c-117">This parameter is required.</span></span>

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

### <span data-ttu-id="f457c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f457c-118">-DefaultProfile</span></span>
<span data-ttu-id="f457c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f457c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f457c-120">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="f457c-120">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="f457c-121">Identyfikator konfiguracji nazwy hosta.</span><span class="sxs-lookup"><span data-stu-id="f457c-121">Hostname Configuration identifier.</span></span>
<span data-ttu-id="f457c-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f457c-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="f457c-123">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="f457c-123">-GatewayId</span></span>
<span data-ttu-id="f457c-124">Identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="f457c-124">Gateway identifier.</span></span>
<span data-ttu-id="f457c-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f457c-125">This parameter is required.</span></span>

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

### <span data-ttu-id="f457c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f457c-126">CommonParameters</span></span>
<span data-ttu-id="f457c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f457c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f457c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f457c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f457c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f457c-129">INPUTS</span></span>

### <span data-ttu-id="f457c-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f457c-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f457c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f457c-131">System.String</span></span>

## <span data-ttu-id="f457c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f457c-132">OUTPUTS</span></span>

### <span data-ttu-id="f457c-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f457c-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="f457c-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f457c-134">NOTES</span></span>

## <span data-ttu-id="f457c-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f457c-135">RELATED LINKS</span></span>
