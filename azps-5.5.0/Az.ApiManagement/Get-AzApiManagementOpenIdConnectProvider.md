---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6968b4ea1b222d0f046611f10e65f8073a4ba86a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192515"
---
# <span data-ttu-id="5a757-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5a757-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5a757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a757-102">SYNOPSIS</span></span>
<span data-ttu-id="5a757-103">Pobiera dostawców usługi OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="5a757-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="5a757-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5a757-104">SYNTAX</span></span>

### <span data-ttu-id="5a757-105">GetAllOpenIdConnectProviders (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5a757-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a757-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5a757-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a757-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="5a757-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a757-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5a757-108">DESCRIPTION</span></span>
<span data-ttu-id="5a757-109">Polecenie **cmdlet Get-AzApiManagementOpenIdConnectProvider** pobiera dostawców połączenia OpenID w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="5a757-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>
<span data-ttu-id="5a757-110">ClientSecret nie zostanie uwzględniony w szczegółach wyników.</span><span class="sxs-lookup"><span data-stu-id="5a757-110">ClientSecret will not be included into result details.</span></span> <span data-ttu-id="5a757-111">Aby uzyskać klucz tajny klienta, użyj funkcji **Get-AzApiManagementOpenIdConnectProviderClientSecret.**</span><span class="sxs-lookup"><span data-stu-id="5a757-111">To get client secret, use **Get-AzApiManagementOpenIdConnectProviderClientSecret**.</span></span>

## <span data-ttu-id="5a757-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5a757-112">EXAMPLES</span></span>

### <span data-ttu-id="5a757-113">Przykład 1. Pobierz wszystkich dostawców</span><span class="sxs-lookup"><span data-stu-id="5a757-113">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="5a757-114">To polecenie pobiera wszystkich dostawców połączenia OpenID w określonym kontekście.</span><span class="sxs-lookup"><span data-stu-id="5a757-114">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="5a757-115">Przykład 2. Uzyskiwanie dostawcy przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="5a757-115">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="5a757-116">To polecenie pobiera dostawcę, który ma identyfikator OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="5a757-116">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="5a757-117">Przykład 3. Uzyskiwanie dostawcy przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="5a757-117">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="5a757-118">To polecenie pobiera dostawcę o nazwie Contoso OpenID Connect Provider.</span><span class="sxs-lookup"><span data-stu-id="5a757-118">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="5a757-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a757-119">PARAMETERS</span></span>

### <span data-ttu-id="5a757-120">— kontekst</span><span class="sxs-lookup"><span data-stu-id="5a757-120">-Context</span></span>
<span data-ttu-id="5a757-121">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="5a757-121">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5a757-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a757-122">-DefaultProfile</span></span>
<span data-ttu-id="5a757-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a757-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a757-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5a757-124">-Name</span></span>
<span data-ttu-id="5a757-125">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="5a757-125">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="5a757-126">Jeśli określisz nazwę, to polecenie cmdlet pobiera tego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="5a757-126">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a757-127">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5a757-127">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5a757-128">Określa identyfikator dostawcy, który usuwa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a757-128">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="5a757-129">Jeśli określisz identyfikator, to polecenie cmdlet pobiera tego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="5a757-129">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a757-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a757-130">CommonParameters</span></span>
<span data-ttu-id="5a757-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a757-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a757-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a757-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a757-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a757-133">INPUTS</span></span>

### <span data-ttu-id="5a757-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5a757-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5a757-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5a757-135">System.String</span></span>

## <span data-ttu-id="5a757-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a757-136">OUTPUTS</span></span>

### <span data-ttu-id="5a757-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5a757-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5a757-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5a757-138">NOTES</span></span>

## <span data-ttu-id="5a757-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a757-139">RELATED LINKS</span></span>

[<span data-ttu-id="5a757-140">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5a757-140">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5a757-141">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5a757-141">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5a757-142">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5a757-142">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


