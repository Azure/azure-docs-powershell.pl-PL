---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: b39ae66a5881acca72143274c479685ef1282854
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052843"
---
# <span data-ttu-id="c89ff-101">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c89ff-101">Get-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c89ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c89ff-102">SYNOPSIS</span></span>
<span data-ttu-id="c89ff-103">Pobiera dostawców z OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="c89ff-103">Gets OpenID Connect providers.</span></span>

## <span data-ttu-id="c89ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c89ff-104">SYNTAX</span></span>

### <span data-ttu-id="c89ff-105">GetAllOpenIdConnectProviders (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c89ff-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c89ff-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="c89ff-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c89ff-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="c89ff-107">GetByName</span></span>
```
Get-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c89ff-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c89ff-108">DESCRIPTION</span></span>
<span data-ttu-id="c89ff-109">Polecenie cmdlet **Get-AzApiManagementOpenIdConnectProvider** Pobiera dostawców usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="c89ff-109">The **Get-AzApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="c89ff-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c89ff-110">EXAMPLES</span></span>

### <span data-ttu-id="c89ff-111">Przykład 1: Pobierz wszystkich dostawców</span><span class="sxs-lookup"><span data-stu-id="c89ff-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="c89ff-112">To polecenie pobiera wszystkich dostawców usługi OpenID Connect dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="c89ff-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="c89ff-113">Przykład 2: Uzyskaj dostawcę przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="c89ff-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01"
```

<span data-ttu-id="c89ff-114">To polecenie uzyskuje dostawcę o IDENTYFIKATORze OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="c89ff-114">This command gets the provider that has the ID OICProvider01.</span></span>

### <span data-ttu-id="c89ff-115">Przykład 3: Uzyskaj dostawcę przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="c89ff-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="c89ff-116">To polecenie uzyskuje dostawcę o nazwie contoso OpenID Connect Provider.</span><span class="sxs-lookup"><span data-stu-id="c89ff-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="c89ff-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c89ff-117">PARAMETERS</span></span>

### <span data-ttu-id="c89ff-118">-Context</span><span class="sxs-lookup"><span data-stu-id="c89ff-118">-Context</span></span>
<span data-ttu-id="c89ff-119">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c89ff-119">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c89ff-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c89ff-120">-DefaultProfile</span></span>
<span data-ttu-id="c89ff-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c89ff-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c89ff-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c89ff-122">-Name</span></span>
<span data-ttu-id="c89ff-123">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="c89ff-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="c89ff-124">Jeśli określisz nazwę, to polecenie cmdlet otrzyma tego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="c89ff-124">If you specify a name, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="c89ff-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="c89ff-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="c89ff-126">Określa identyfikator dostawcy, który usunie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c89ff-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="c89ff-127">Jeśli określisz identyfikator, to polecenie cmdlet otrzyma tego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="c89ff-127">If you specify an ID, this cmdlet gets that provider.</span></span>

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

### <span data-ttu-id="c89ff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c89ff-128">CommonParameters</span></span>
<span data-ttu-id="c89ff-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c89ff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c89ff-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c89ff-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c89ff-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c89ff-131">INPUTS</span></span>

### <span data-ttu-id="c89ff-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c89ff-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c89ff-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c89ff-133">System.String</span></span>

## <span data-ttu-id="c89ff-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c89ff-134">OUTPUTS</span></span>

### <span data-ttu-id="c89ff-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c89ff-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="c89ff-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c89ff-136">NOTES</span></span>

## <span data-ttu-id="c89ff-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c89ff-137">RELATED LINKS</span></span>

[<span data-ttu-id="c89ff-138">Nowe — AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c89ff-138">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c89ff-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c89ff-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="c89ff-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="c89ff-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


