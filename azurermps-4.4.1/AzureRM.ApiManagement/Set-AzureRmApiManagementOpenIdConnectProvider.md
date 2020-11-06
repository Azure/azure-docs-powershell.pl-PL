---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: f890236907ea0a717245d9345be276a6ccf04b8c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548416"
---
# <span data-ttu-id="bfa08-101">Set-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bfa08-101">Set-AzureRmApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bfa08-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bfa08-102">SYNOPSIS</span></span>
<span data-ttu-id="bfa08-103">Modyfikuje dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="bfa08-103">Modifies an OpenID Connect provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfa08-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bfa08-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOpenIdConnectProvider -Context <PsApiManagementContext>
 -OpenIdConnectProviderId <String> [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>]
 [-ClientSecret <String>] [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfa08-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bfa08-105">DESCRIPTION</span></span>
<span data-ttu-id="bfa08-106">Polecenie cmdlet **Set-AzureRmApiManagementOpenIdConnectProvider** modyfikuje dostawcę usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="bfa08-106">The **Set-AzureRmApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="bfa08-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bfa08-107">EXAMPLES</span></span>

### <span data-ttu-id="bfa08-108">Przykład 1. Zmienianie klucza tajnego klienta dla dostawcy</span><span class="sxs-lookup"><span data-stu-id="bfa08-108">Example 1: Change the client secret for a provider</span></span>
```
PS C:\>Set-AzureRmApiManagementOpenIdConnectProvider -Context $ApimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="bfa08-109">To polecenie modyfikuje dostawcę o IDENTYFIKATORze OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="bfa08-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="bfa08-110">To polecenie określa klucz tajny klienta dla dostawcy.</span><span class="sxs-lookup"><span data-stu-id="bfa08-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="bfa08-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfa08-111">PARAMETERS</span></span>

### <span data-ttu-id="bfa08-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="bfa08-112">-ClientId</span></span>
<span data-ttu-id="bfa08-113">Określa identyfikator klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="bfa08-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="bfa08-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="bfa08-114">-ClientSecret</span></span>
<span data-ttu-id="bfa08-115">Określa klucz tajny klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="bfa08-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="bfa08-116">-Context</span><span class="sxs-lookup"><span data-stu-id="bfa08-116">-Context</span></span>
<span data-ttu-id="bfa08-117">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="bfa08-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bfa08-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="bfa08-118">-Description</span></span>
<span data-ttu-id="bfa08-119">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="bfa08-119">Specifies a description.</span></span>

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

### <span data-ttu-id="bfa08-120">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="bfa08-120">-MetadataEndpointUri</span></span>
<span data-ttu-id="bfa08-121">Określa identyfikator URI punktu końcowego metadanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="bfa08-121">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="bfa08-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bfa08-122">-Name</span></span>
<span data-ttu-id="bfa08-123">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="bfa08-123">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="bfa08-124">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="bfa08-124">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="bfa08-125">Określa identyfikator dostawcy, który modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa08-125">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="bfa08-126">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="bfa08-126">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="bfa08-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfa08-127">-PassThru</span></span>
<span data-ttu-id="bfa08-128">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementOpenIdConnectProvider** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bfa08-128">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="bfa08-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfa08-129">-DefaultProfile</span></span>
<span data-ttu-id="bfa08-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfa08-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bfa08-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfa08-131">CommonParameters</span></span>
<span data-ttu-id="bfa08-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfa08-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfa08-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfa08-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfa08-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfa08-134">INPUTS</span></span>

## <span data-ttu-id="bfa08-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bfa08-135">OUTPUTS</span></span>

### <span data-ttu-id="bfa08-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bfa08-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="bfa08-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bfa08-137">NOTES</span></span>

## <span data-ttu-id="bfa08-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfa08-138">RELATED LINKS</span></span>

[<span data-ttu-id="bfa08-139">Get-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bfa08-139">Get-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Get-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bfa08-140">Nowe — AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bfa08-140">New-AzureRmApiManagementOpenIdConnectProvider</span></span>](./New-AzureRmApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="bfa08-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="bfa08-141">Remove-AzureRmApiManagementOpenIdConnectProvider</span></span>](./Remove-AzureRmApiManagementOpenIdConnectProvider.md)


