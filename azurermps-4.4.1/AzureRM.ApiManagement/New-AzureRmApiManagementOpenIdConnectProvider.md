---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f008d21e1d1d3f2aba7c87255fa7c95074bca532
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547196"
---
# <span data-ttu-id="682fa-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="682fa-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="682fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="682fa-102">SYNOPSIS</span></span>
<span data-ttu-id="682fa-103">Tworzy dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="682fa-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="682fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="682fa-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="682fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="682fa-105">DESCRIPTION</span></span>
<span data-ttu-id="682fa-106">Polecenie cmdlet **New-AzureRmApiManagementOpenIdConnectProvider** umożliwia utworzenie dostawcy usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="682fa-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="682fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="682fa-107">EXAMPLES</span></span>

### <span data-ttu-id="682fa-108">Przykład 1: Tworzenie dostawcy</span><span class="sxs-lookup"><span data-stu-id="682fa-108">Example 1: Create a provider</span></span>
```
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="682fa-109">To polecenie tworzy **dostawcę** OpenID Connect o nazwie contoso OpenID Connect Provider</span><span class="sxs-lookup"><span data-stu-id="682fa-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="682fa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="682fa-110">PARAMETERS</span></span>

### <span data-ttu-id="682fa-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="682fa-111">-ClientId</span></span>
<span data-ttu-id="682fa-112">Określa identyfikator klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="682fa-112">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="682fa-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="682fa-113">-ClientSecret</span></span>
<span data-ttu-id="682fa-114">Określa klucz tajny klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="682fa-114">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="682fa-115">-Context</span><span class="sxs-lookup"><span data-stu-id="682fa-115">-Context</span></span>
<span data-ttu-id="682fa-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="682fa-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="682fa-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="682fa-117">-Description</span></span>
<span data-ttu-id="682fa-118">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="682fa-118">Specifies a description.</span></span>

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

### <span data-ttu-id="682fa-119">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="682fa-119">-MetadataEndpointUri</span></span>
<span data-ttu-id="682fa-120">Określa identyfikator URI punktu końcowego metadanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="682fa-120">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="682fa-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="682fa-121">-Name</span></span>
<span data-ttu-id="682fa-122">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="682fa-122">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="682fa-123">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="682fa-123">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="682fa-124">Określa identyfikator dostawcy.</span><span class="sxs-lookup"><span data-stu-id="682fa-124">Specifies an ID for the provider.</span></span>
<span data-ttu-id="682fa-125">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="682fa-125">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="682fa-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="682fa-126">-DefaultProfile</span></span>
<span data-ttu-id="682fa-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="682fa-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="682fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="682fa-128">CommonParameters</span></span>
<span data-ttu-id="682fa-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="682fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="682fa-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="682fa-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="682fa-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="682fa-131">INPUTS</span></span>

## <span data-ttu-id="682fa-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="682fa-132">OUTPUTS</span></span>

### <span data-ttu-id="682fa-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="682fa-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="682fa-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="682fa-134">NOTES</span></span>

## <span data-ttu-id="682fa-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="682fa-135">RELATED LINKS</span></span>

[<span data-ttu-id="682fa-136">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="682fa-136">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="682fa-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="682fa-137">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="682fa-138">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="682fa-138">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


