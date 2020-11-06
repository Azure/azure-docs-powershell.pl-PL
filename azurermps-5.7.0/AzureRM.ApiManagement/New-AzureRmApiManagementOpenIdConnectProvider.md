---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: D5B18FF4-3294-4561-A4CD-CF0FA5E4A59B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 088b88bcaa7f0d493552060c150e9d76a4b16c7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525409"
---
# <span data-ttu-id="5fb6f-101">New-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fb6f-101">New-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5fb6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5fb6f-102">SYNOPSIS</span></span>
<span data-ttu-id="5fb6f-103">Tworzy dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-103">Creates an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fb6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5fb6f-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 [-OpenIdConnectProviderId <String>] -Name <String> -MetadataEndpointUri <String> -ClientId <String>
 [-ClientSecret <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5fb6f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5fb6f-105">DESCRIPTION</span></span>
<span data-ttu-id="5fb6f-106">Polecenie cmdlet **New-AzureRmApiManagementOpenIdConnectProvider** umożliwia utworzenie dostawcy usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-106">The **New-AzureRmApiManagementOpenIdConnectProvider** cmdlet creates an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="5fb6f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5fb6f-107">EXAMPLES</span></span>

### <span data-ttu-id="5fb6f-108">Przykład 1: Tworzenie dostawcy</span><span class="sxs-lookup"><span data-stu-id="5fb6f-108">Example 1: Create a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -Name "Contoso OpenID Connect Provider" -MetadataEndpointUri "https://openid.provider/configuration" -ClientId "12432143" -Description "OpenID Connect provider description"
```

<span data-ttu-id="5fb6f-109">To polecenie tworzy **dostawcę** OpenID Connect o nazwie contoso OpenID Connect Provider</span><span class="sxs-lookup"><span data-stu-id="5fb6f-109">This command creates an OpenID Connect **Provider** named Contoso OpenID Connect Provider</span></span>

## <span data-ttu-id="5fb6f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5fb6f-110">PARAMETERS</span></span>

### <span data-ttu-id="5fb6f-111">-ClientId</span><span class="sxs-lookup"><span data-stu-id="5fb6f-111">-ClientId</span></span>
<span data-ttu-id="5fb6f-112">Określa identyfikator klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-112">Specifies the client ID of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb6f-113">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="5fb6f-113">-ClientSecret</span></span>
<span data-ttu-id="5fb6f-114">Określa klucz tajny klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-114">Specifies the client secret of the developer console.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb6f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="5fb6f-115">-Context</span></span>
<span data-ttu-id="5fb6f-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="5fb6f-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5fb6f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fb6f-117">-DefaultProfile</span></span>
<span data-ttu-id="5fb6f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="5fb6f-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="5fb6f-119">-Description</span></span>
<span data-ttu-id="5fb6f-120">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-120">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb6f-121">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="5fb6f-121">-MetadataEndpointUri</span></span>
<span data-ttu-id="5fb6f-122">Określa identyfikator URI punktu końcowego metadanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-122">Specifies a metadata endpoint URI of the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb6f-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5fb6f-123">-Name</span></span>
<span data-ttu-id="5fb6f-124">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-124">Specifies a friendly name for the provider.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb6f-125">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="5fb6f-125">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="5fb6f-126">Określa identyfikator dostawcy.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-126">Specifies an ID for the provider.</span></span>
<span data-ttu-id="5fb6f-127">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-127">If you do not specify an ID, this cmdlet generates one.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5fb6f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fb6f-128">CommonParameters</span></span>
<span data-ttu-id="5fb6f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fb6f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fb6f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fb6f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5fb6f-131">INPUTS</span></span>

### <span data-ttu-id="5fb6f-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5fb6f-132">None</span></span>
<span data-ttu-id="5fb6f-133">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5fb6f-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5fb6f-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5fb6f-134">OUTPUTS</span></span>

### <span data-ttu-id="5fb6f-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fb6f-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="5fb6f-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5fb6f-136">NOTES</span></span>

## <span data-ttu-id="5fb6f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5fb6f-137">RELATED LINKS</span></span>

[<span data-ttu-id="5fb6f-138">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fb6f-138">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5fb6f-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fb6f-139">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="5fb6f-140">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="5fb6f-140">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Set-AzureRmApiManagementOpenIdConnectProvider.md)


