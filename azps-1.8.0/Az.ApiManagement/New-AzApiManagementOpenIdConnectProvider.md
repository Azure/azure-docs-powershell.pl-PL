---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 3b4cec203e39401885874db5391f62a9f1663342
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869504"
---
# <span data-ttu-id="6a728-101">New-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6a728-101">New-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="6a728-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a728-102">SYNOPSIS</span></span>
<span data-ttu-id="6a728-103">Tworzy dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="6a728-103">Creates an OpenID Connect provider.</span></span>

## <span data-ttu-id="6a728-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a728-104">SYNTAX</span></span>

```
New-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> [-OpenIdConnectProviderId <String>]
 -Name <String> -MetadataEndpointUri <String> -ClientId <String> [-ClientSecret <String>]
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a728-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a728-105">DESCRIPTION</span></span>
<span data-ttu-id="6a728-106">Polecenie cmdlet **New-AzApiManagementOpenIdConnectProvider** umożliwia utworzenie dostawcy usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="6a728-106">The **New-AzApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="6a728-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a728-107">EXAMPLES</span></span>

### <span data-ttu-id="6a728-108">Przykład 1: Tworzenie dostawcy</span><span class="sxs-lookup"><span data-stu-id="6a728-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="6a728-109">To polecenie tworzy **dostawcę** OpenID Connect o nazwie contoso OpenID Connect Provider</span><span class="sxs-lookup"><span data-stu-id="6a728-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="6a728-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a728-110">PARAMETERS</span></span>

### <span data-ttu-id="6a728-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="6a728-111">-ClientId</span></span>
<span data-ttu-id="6a728-112">Określa identyfikator klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="6a728-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="6a728-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="6a728-113">-ClientSecret</span></span>
<span data-ttu-id="6a728-114">Określa klucz tajny klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="6a728-114">Specifies the client secret of the developer console.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a728-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6a728-115">-Context</span></span>
<span data-ttu-id="6a728-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="6a728-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="6a728-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a728-117">-DefaultProfile</span></span>
<span data-ttu-id="6a728-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a728-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a728-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="6a728-119">-Description</span></span>
<span data-ttu-id="6a728-120">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="6a728-120">Specifies a description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a728-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="6a728-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="6a728-122">Określa identyfikator URI punktu końcowego metadanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="6a728-122">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="6a728-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6a728-123">-Name</span></span>
<span data-ttu-id="6a728-124">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="6a728-124">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="6a728-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="6a728-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="6a728-126">Określa identyfikator dostawcy.</span><span class="sxs-lookup"><span data-stu-id="6a728-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="6a728-127">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="6a728-127">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a728-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a728-128">CommonParameters</span></span>
<span data-ttu-id="6a728-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a728-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a728-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a728-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a728-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a728-131">INPUTS</span></span>

### <span data-ttu-id="6a728-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6a728-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6a728-133">System. String</span><span class="sxs-lookup"><span data-stu-id="6a728-133">System.String</span></span>

## <span data-ttu-id="6a728-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a728-134">OUTPUTS</span></span>

### <span data-ttu-id="6a728-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6a728-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="6a728-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a728-136">NOTES</span></span>

## <span data-ttu-id="6a728-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a728-137">RELATED LINKS</span></span>

[<span data-ttu-id="6a728-138">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6a728-138">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="6a728-139">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6a728-139">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="6a728-140">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="6a728-140">Set-AzApiManagementOpenIdConnectProvider</span></span>](./Set-AzApiManagementOpenIdConnectProvider.md)


