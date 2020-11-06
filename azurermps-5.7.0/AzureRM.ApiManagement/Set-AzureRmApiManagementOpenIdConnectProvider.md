---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: c914c49aeb4f2a763a09c5b513bcbe7809110b05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553699"
---
# <span data-ttu-id="f1ddc-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1ddc-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f1ddc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1ddc-102">SYNOPSIS</span></span>
<span data-ttu-id="f1ddc-103">Modyfikuje dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1ddc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1ddc-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1ddc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f1ddc-105">DESCRIPTION</span></span>
<span data-ttu-id="f1ddc-106">Polecenie cmdlet **Set-AzureRmApiManagementOpenIdConnectProvider** modyfikuje dostawcę usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="f1ddc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1ddc-107">EXAMPLES</span></span>

### <span data-ttu-id="f1ddc-108">Przykład 1. Zmienianie klucza tajnego klienta dla dostawcy</span><span class="sxs-lookup"><span data-stu-id="f1ddc-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="f1ddc-109">To polecenie modyfikuje dostawcę o IDENTYFIKATORze OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="f1ddc-110">To polecenie określa klucz tajny klienta dla dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="f1ddc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1ddc-111">PARAMETERS</span></span>

### <span data-ttu-id="f1ddc-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f1ddc-112">-ClientId</span></span>
<span data-ttu-id="f1ddc-113">Określa identyfikator klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="f1ddc-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f1ddc-114">-ClientSecret</span></span>
<span data-ttu-id="f1ddc-115">Określa klucz tajny klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="f1ddc-116">-Context</span><span class="sxs-lookup"><span data-stu-id="f1ddc-116">-Context</span></span>
<span data-ttu-id="f1ddc-117">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f1ddc-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f1ddc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1ddc-118">-DefaultProfile</span></span>
<span data-ttu-id="f1ddc-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="f1ddc-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="f1ddc-120">-Description</span></span>
<span data-ttu-id="f1ddc-121">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-121">Specifies a description.</span></span>

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

### <span data-ttu-id="f1ddc-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="f1ddc-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="f1ddc-123">Określa identyfikator URI punktu końcowego metadanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="f1ddc-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f1ddc-124">-Name</span></span>
<span data-ttu-id="f1ddc-125">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="f1ddc-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="f1ddc-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="f1ddc-127">Określa identyfikator dostawcy, który modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="f1ddc-128">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="f1ddc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f1ddc-129">-PassThru</span></span>
<span data-ttu-id="f1ddc-130">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementOpenIdConnectProvider** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1ddc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1ddc-131">CommonParameters</span></span>
<span data-ttu-id="f1ddc-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1ddc-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1ddc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1ddc-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1ddc-134">INPUTS</span></span>

### <span data-ttu-id="f1ddc-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="f1ddc-135">None</span></span>
<span data-ttu-id="f1ddc-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="f1ddc-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f1ddc-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1ddc-137">OUTPUTS</span></span>

### <span data-ttu-id="f1ddc-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1ddc-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f1ddc-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1ddc-139">NOTES</span></span>

## <span data-ttu-id="f1ddc-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1ddc-140">RELATED LINKS</span></span>

[<span data-ttu-id="f1ddc-141">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1ddc-141">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f1ddc-142">Nowe — AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1ddc-142">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f1ddc-143">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f1ddc-143">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


