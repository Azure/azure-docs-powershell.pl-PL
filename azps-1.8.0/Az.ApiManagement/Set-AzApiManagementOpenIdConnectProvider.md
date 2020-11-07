---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: fe320af601fad9d905471525b1a418c12c355f63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869336"
---
# <span data-ttu-id="07c80-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="07c80-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="07c80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="07c80-102">SYNOPSIS</span></span>
<span data-ttu-id="07c80-103">Modyfikuje dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="07c80-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="07c80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="07c80-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07c80-105">Opis</span><span class="sxs-lookup"><span data-stu-id="07c80-105">DESCRIPTION</span></span>
<span data-ttu-id="07c80-106">Polecenie cmdlet **Set-AzApiManagementOpenIdConnectProvider** modyfikuje dostawcę usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="07c80-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="07c80-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="07c80-107">EXAMPLES</span></span>

### <span data-ttu-id="07c80-108">Przykład 1. Zmienianie klucza tajnego klienta dla dostawcy</span><span class="sxs-lookup"><span data-stu-id="07c80-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvicer01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="07c80-109">To polecenie modyfikuje dostawcę o IDENTYFIKATORze OICProvicer01.</span><span class="sxs-lookup"><span data-stu-id="07c80-109">This command modifies the provider that has the ID OICProvicer01.</span></span>
<span data-ttu-id="07c80-110">To polecenie określa klucz tajny klienta dla dostawcy.</span><span class="sxs-lookup"><span data-stu-id="07c80-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="07c80-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="07c80-111">PARAMETERS</span></span>

### <span data-ttu-id="07c80-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="07c80-112">-ClientId</span></span>
<span data-ttu-id="07c80-113">Określa identyfikator klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="07c80-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="07c80-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="07c80-114">-ClientSecret</span></span>
<span data-ttu-id="07c80-115">Określa klucz tajny klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="07c80-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="07c80-116">-Context</span><span class="sxs-lookup"><span data-stu-id="07c80-116">-Context</span></span>
<span data-ttu-id="07c80-117">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="07c80-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="07c80-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07c80-118">-DefaultProfile</span></span>
<span data-ttu-id="07c80-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="07c80-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07c80-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="07c80-120">-Description</span></span>
<span data-ttu-id="07c80-121">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="07c80-121">Specifies a description.</span></span>

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

### <span data-ttu-id="07c80-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="07c80-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="07c80-123">Określa identyfikator URI punktu końcowego metadanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="07c80-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="07c80-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="07c80-124">-Name</span></span>
<span data-ttu-id="07c80-125">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="07c80-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="07c80-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="07c80-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="07c80-127">Określa identyfikator dostawcy, który modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07c80-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="07c80-128">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="07c80-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="07c80-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07c80-129">-PassThru</span></span>
<span data-ttu-id="07c80-130">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementOpenIdConnectProvider** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07c80-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="07c80-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07c80-131">CommonParameters</span></span>
<span data-ttu-id="07c80-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07c80-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07c80-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07c80-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07c80-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="07c80-134">INPUTS</span></span>

### <span data-ttu-id="07c80-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="07c80-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="07c80-136">System. String</span><span class="sxs-lookup"><span data-stu-id="07c80-136">System.String</span></span>

### <span data-ttu-id="07c80-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="07c80-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="07c80-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="07c80-138">OUTPUTS</span></span>

### <span data-ttu-id="07c80-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="07c80-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="07c80-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="07c80-140">NOTES</span></span>

## <span data-ttu-id="07c80-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="07c80-141">RELATED LINKS</span></span>

[<span data-ttu-id="07c80-142">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="07c80-142">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="07c80-143">Nowe — AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="07c80-143">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="07c80-144">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="07c80-144">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


