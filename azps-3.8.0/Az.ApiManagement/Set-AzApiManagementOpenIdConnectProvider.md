---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F3F21304-CED1-4742-B8BD-2841C4107DCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementopenidconnectprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOpenIdConnectProvider.md
ms.openlocfilehash: 4bceb472fb3971b177f53b43fc48ad00c1422b58
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053147"
---
# <span data-ttu-id="f3b3a-101">Set-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f3b3a-101">Set-AzApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f3b3a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b3a-103">Modyfikuje dostawcę OpenID Connect.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-103">Modifies an OpenID Connect provider.</span></span>

## <span data-ttu-id="f3b3a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3b3a-104">SYNTAX</span></span>

```
Set-AzApiManagementOpenIdConnectProvider -Context <PsApiManagementContext> -OpenIdConnectProviderId <String>
 [-Name <String>] [-MetadataEndpointUri <String>] [-ClientId <String>] [-ClientSecret <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3b3a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3b3a-105">DESCRIPTION</span></span>
<span data-ttu-id="f3b3a-106">Polecenie cmdlet **Set-AzApiManagementOpenIdConnectProvider** modyfikuje dostawcę usługi OpenID Connect w usłudze Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-106">The **Set-AzApiManagementOpenIdConnectProvider** cmdlet modifies an OpenID Connect provider in Azure API Management.</span></span>

## <span data-ttu-id="f3b3a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3b3a-107">EXAMPLES</span></span>

### <span data-ttu-id="f3b3a-108">Przykład 1. Zmienianie klucza tajnego klienta dla dostawcy</span><span class="sxs-lookup"><span data-stu-id="f3b3a-108">Example 1: Change the client secret for a provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementOpenIdConnectProvider -Context $apimContext -OpenIdConnectProviderId "OICProvider01" -ClientSecret "q2w3e43r45" -PassThru
```

<span data-ttu-id="f3b3a-109">To polecenie modyfikuje dostawcę o IDENTYFIKATORze OICProvider01.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-109">This command modifies the provider that has the ID OICProvider01.</span></span>
<span data-ttu-id="f3b3a-110">To polecenie określa klucz tajny klienta dla dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-110">The command specifies a client secret for the provider.</span></span>

## <span data-ttu-id="f3b3a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3b3a-111">PARAMETERS</span></span>

### <span data-ttu-id="f3b3a-112">-ClientId</span><span class="sxs-lookup"><span data-stu-id="f3b3a-112">-ClientId</span></span>
<span data-ttu-id="f3b3a-113">Określa identyfikator klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-113">Specifies the client ID of the developer console.</span></span>

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

### <span data-ttu-id="f3b3a-114">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="f3b3a-114">-ClientSecret</span></span>
<span data-ttu-id="f3b3a-115">Określa klucz tajny klienta konsoli dewelopera.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-115">Specifies the client secret of the developer console.</span></span>

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

### <span data-ttu-id="f3b3a-116">-Context</span><span class="sxs-lookup"><span data-stu-id="f3b3a-116">-Context</span></span>
<span data-ttu-id="f3b3a-117">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="f3b3a-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f3b3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3b3a-118">-DefaultProfile</span></span>
<span data-ttu-id="f3b3a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3b3a-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="f3b3a-120">-Description</span></span>
<span data-ttu-id="f3b3a-121">Określa opis.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-121">Specifies a description.</span></span>

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

### <span data-ttu-id="f3b3a-122">-MetadataEndpointUri</span><span class="sxs-lookup"><span data-stu-id="f3b3a-122">-MetadataEndpointUri</span></span>
<span data-ttu-id="f3b3a-123">Określa identyfikator URI punktu końcowego metadanych dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-123">Specifies a metadata endpoint URI of the provider.</span></span>

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

### <span data-ttu-id="f3b3a-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3b3a-124">-Name</span></span>
<span data-ttu-id="f3b3a-125">Określa przyjazną nazwę dostawcy.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-125">Specifies a friendly name for the provider.</span></span>

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

### <span data-ttu-id="f3b3a-126">-OpenIdConnectProviderId</span><span class="sxs-lookup"><span data-stu-id="f3b3a-126">-OpenIdConnectProviderId</span></span>
<span data-ttu-id="f3b3a-127">Określa identyfikator dostawcy, który modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-127">Specifies an ID for the provider that this cmdlet modifies.</span></span>
<span data-ttu-id="f3b3a-128">Jeśli nie określisz identyfikatora, to polecenie cmdlet wygeneruje je.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-128">If you do not specify an ID, this cmdlet generates one.</span></span>

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

### <span data-ttu-id="f3b3a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3b3a-129">-PassThru</span></span>
<span data-ttu-id="f3b3a-130">Wskazuje, że to polecenie cmdlet zwróci **PsApiManagementOpenIdConnectProvider** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-130">Indicates that this cmdlet returns the **PsApiManagementOpenIdConnectProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f3b3a-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3b3a-131">-Confirm</span></span>
<span data-ttu-id="f3b3a-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b3a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b3a-133">-WhatIf</span></span>
<span data-ttu-id="f3b3a-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3b3a-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b3a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b3a-136">CommonParameters</span></span>
<span data-ttu-id="f3b3a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3b3a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b3a-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3b3a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b3a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3b3a-139">INPUTS</span></span>

### <span data-ttu-id="f3b3a-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f3b3a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f3b3a-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f3b3a-141">System.String</span></span>

### <span data-ttu-id="f3b3a-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f3b3a-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f3b3a-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3b3a-143">OUTPUTS</span></span>

### <span data-ttu-id="f3b3a-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f3b3a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOpenIdConnectProvider</span></span>

## <span data-ttu-id="f3b3a-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3b3a-145">NOTES</span></span>

## <span data-ttu-id="f3b3a-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3b3a-146">RELATED LINKS</span></span>

[<span data-ttu-id="f3b3a-147">Get-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f3b3a-147">Get-AzApiManagementOpenIdConnectProvider</span></span>](./Get-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f3b3a-148">Nowe — AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f3b3a-148">New-AzApiManagementOpenIdConnectProvider</span></span>](./New-AzApiManagementOpenIdConnectProvider.md)

[<span data-ttu-id="f3b3a-149">Remove-AzApiManagementOpenIdConnectProvider</span><span class="sxs-lookup"><span data-stu-id="f3b3a-149">Remove-AzApiManagementOpenIdConnectProvider</span></span>](./Remove-AzApiManagementOpenIdConnectProvider.md)


