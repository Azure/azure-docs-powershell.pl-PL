---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 6f568f27cf5b50cd517d8133578d6cf36060252f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526397"
---
# <span data-ttu-id="36295-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="36295-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="36295-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36295-102">SYNOPSIS</span></span>
<span data-ttu-id="36295-103">Modyfikuje dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="36295-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36295-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36295-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36295-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36295-105">DESCRIPTION</span></span>
<span data-ttu-id="36295-106">Polecenie cmdlet **Set-AzureRmApiManagementOpenIdConnectProvider** modyfikuje dostawcę usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="36295-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="36295-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36295-107">EXAMPLES</span></span>

### <span data-ttu-id="36295-108">Przykład 1. Zmienianie klucza tajnego klienta dla dostawcy</span><span class="sxs-lookup"><span data-stu-id="36295-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="36295-109">To polecenie modyfikuje dostawcę o IDENTYFIKATORze OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="36295-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="36295-110">To polecenie określa klucz tajny klienta dla dostawcy.</span><span class="sxs-lookup"><span data-stu-id="36295-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="36295-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36295-111">PARAMETERS</span></span>

### <span data-ttu-id="36295-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="36295-112">-ClientId</span></span>
<span data-ttu-id="36295-113">Określa identyfikator klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="36295-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="36295-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="36295-114">-ClientSecret</span></span>
<span data-ttu-id="36295-115">Określa klucz tajny klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="36295-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="36295-116">-Context</span><span class="sxs-lookup"><span data-stu-id="36295-116">-Context</span></span>
<span data-ttu-id="36295-117">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="36295-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="36295-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36295-118">-DefaultProfile</span></span>
<span data-ttu-id="36295-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="36295-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36295-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="36295-120">-Description</span></span>
<span data-ttu-id="36295-121">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="36295-121">Specifies a description.</span></span>

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

### <span data-ttu-id="36295-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="36295-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="36295-123">Określa identyfikator URI punktu końcowego metadanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="36295-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="36295-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36295-124">-Name</span></span>
<span data-ttu-id="36295-125">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="36295-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="36295-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="36295-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="36295-127">Określa identyfikator dostawcy, który modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36295-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="36295-128">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="36295-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="36295-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36295-129">-PassThru</span></span>
<span data-ttu-id="36295-130">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementOpenIdConnectProvider** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36295-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36295-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36295-131">CommonParameters</span></span>
<span data-ttu-id="36295-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36295-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36295-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36295-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36295-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36295-134">INPUTS</span></span>

### <span data-ttu-id="36295-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="36295-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="36295-136">System. String</span><span class="sxs-lookup"><span data-stu-id="36295-136">System.String</span></span>

### <span data-ttu-id="36295-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36295-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36295-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36295-138">OUTPUTS</span></span>

### <span data-ttu-id="36295-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="36295-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="36295-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36295-140">NOTES</span></span>

## <span data-ttu-id="36295-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36295-141">RELATED LINKS</span></span>

[<span data-ttu-id="36295-142">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="36295-142">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="36295-143">Nowe — AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="36295-143">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="36295-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="36295-144">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


