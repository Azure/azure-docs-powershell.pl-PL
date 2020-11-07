---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15B6EAE2-56ED-4A01-B8EA-52B9FCDC1F66
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c26fb8991acc47ab655cb47c44194ca209423a70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718063"
---
# <span data-ttu-id="29982-101">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="29982-101">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="29982-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29982-102">SYNOPSIS</span></span>
<span data-ttu-id="29982-103">Pobiera dostawców z OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="29982-103">Gets OpenID Connect providers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29982-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29982-104">SYNTAX</span></span>

### <span data-ttu-id="29982-105">GetAllOpenIdConnectProviders (domyślny)</span><span class="sxs-lookup"><span data-stu-id="29982-105">GetAllOpenIdConnectProviders (Default)</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29982-106">GetByOpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="29982-106">GetByOpenIdConnectProviderId</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29982-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="29982-107">GetByName</span></span>
```
Get-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29982-108">Opis</span><span class="sxs-lookup"><span data-stu-id="29982-108">DESCRIPTION</span></span>
<span data-ttu-id="29982-109">Polecenie cmdlet **Get-AzureRmApiManagementOpenIdConnectProvider** Pobiera dostawców usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="29982-109">The **Get-AzureRmApiManagementOpenIdConnectProvider** cmdlet gets OpenID Connect providers in Azure API Management.</span></span>

## <span data-ttu-id="29982-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29982-110">EXAMPLES</span></span>

### <span data-ttu-id="29982-111">Przykład 1: Pobierz wszystkich dostawców</span><span class="sxs-lookup"><span data-stu-id="29982-111">Example 1: Get all providers</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext
```

<span data-ttu-id="29982-112">To polecenie pobiera wszystkich dostawców usługi OpenID Connect dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="29982-112">This command gets all OpenID Connect providers for the specified context.</span></span>

### <span data-ttu-id="29982-113">Przykład 2: Uzyskaj dostawcę przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="29982-113">Example 2: Get a provider by using an ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01"
```

<span data-ttu-id="29982-114">To polecenie uzyskuje dostawcę o IDENTYFIKATORze OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="29982-114">This command gets the provider that has the ID OICProvicer01.</span></span>

### <span data-ttu-id="29982-115">Przykład 3: Uzyskaj dostawcę przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="29982-115">Example 3: Get a provider by using a name</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -Name "Contoso OpenID Connect Provider"
```

<span data-ttu-id="29982-116">To polecenie uzyskuje dostawcę o nazwie contoso OpenID Connect Provider.</span><span class="sxs-lookup"><span data-stu-id="29982-116">This command gets the provider named Contoso OpenID Connect Provider.</span></span>

## <span data-ttu-id="29982-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29982-117">PARAMETERS</span></span>

### <span data-ttu-id="29982-118">-Context</span><span class="sxs-lookup"><span data-stu-id="29982-118">-Context</span></span>
<span data-ttu-id="29982-119">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="29982-119">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29982-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29982-120">-DefaultProfile</span></span>
<span data-ttu-id="29982-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="29982-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29982-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29982-122">-Name</span></span>
<span data-ttu-id="29982-123">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="29982-123">Specifies a friendly name of a provider.</span></span>
<span data-ttu-id="29982-124">Jeśli określisz nazwę, to polecenie cmdlet otrzyma tego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="29982-124">If you specify a name, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29982-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="29982-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="29982-126">Określa identyfikator dostawcy, który usunie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29982-126">Specifies an ID of the provider that this cmdlet removes.</span></span>
<span data-ttu-id="29982-127">Jeśli określisz identyfikator, to polecenie cmdlet otrzyma tego dostawcę.</span><span class="sxs-lookup"><span data-stu-id="29982-127">If you specify an ID, this cmdlet gets that provider.</span></span>

```yaml
Type: String
Parameter Sets: GetByOpenIdConnectProviderId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29982-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29982-128">CommonParameters</span></span>
<span data-ttu-id="29982-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29982-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29982-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29982-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29982-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29982-131">INPUTS</span></span>

### <span data-ttu-id="29982-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="29982-132">None</span></span>
<span data-ttu-id="29982-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="29982-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="29982-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29982-134">OUTPUTS</span></span>

### <span data-ttu-id="29982-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="29982-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>
<span data-ttu-id="29982-136">Szczegóły dostawcy OpenId Connect skonfigurowanego w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="29982-136">The detail of the OpenId connect Provider configured in API Management service.</span></span>

### <span data-ttu-id="29982-137">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementOpenIdConnectProvider></span><span class="sxs-lookup"><span data-stu-id="29982-137">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider></span></span>
<span data-ttu-id="29982-138">Lista dostawców usługi OpenId Connect skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="29982-138">The list of OpenId Connect Providers configured in API Management service.</span></span>

## <span data-ttu-id="29982-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29982-139">NOTES</span></span>

## <span data-ttu-id="29982-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29982-140">RELATED LINKS</span></span>

[<span data-ttu-id="29982-141">Nowe — AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="29982-141">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="29982-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="29982-142">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="29982-143">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="29982-143">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


