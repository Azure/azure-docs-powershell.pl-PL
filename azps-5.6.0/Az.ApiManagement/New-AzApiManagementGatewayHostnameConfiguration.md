---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 98e160253db571c32fe14455b8642337029a9707
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965530"
---
# <span data-ttu-id="16117-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="16117-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="16117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16117-102">SYNOPSIS</span></span>
<span data-ttu-id="16117-103">Tworzy nazwę hosta konfiguratin dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="16117-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="16117-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="16117-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16117-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="16117-105">DESCRIPTION</span></span>
<span data-ttu-id="16117-106">Polecenie **cmdlet New-AzApiManagementGatewayHostnameConfiguration** tworzy nazwę hosta konfiguratin dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="16117-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="16117-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="16117-107">EXAMPLES</span></span>

### <span data-ttu-id="16117-108">Przykład 1. Tworzenie konfiguracji nazwy hosta dla istniejącej bramy</span><span class="sxs-lookup"><span data-stu-id="16117-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="16117-109">To polecenie tworzy konfigurację nazwy hosta "h01" dla bramy "g01".</span><span class="sxs-lookup"><span data-stu-id="16117-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="16117-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16117-110">PARAMETERS</span></span>

### <span data-ttu-id="16117-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="16117-111">-CertificateResourceId</span></span>
<span data-ttu-id="16117-112">Identyfikator zasobu dla istniejącego identyfikatora certyfikatu. Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="16117-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="16117-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="16117-113">-Context</span></span>
<span data-ttu-id="16117-114">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="16117-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="16117-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="16117-115">This parameter is required.</span></span>

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

### <span data-ttu-id="16117-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16117-116">-DefaultProfile</span></span>
<span data-ttu-id="16117-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="16117-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16117-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="16117-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="16117-119">Identyfikator pomylinia nazwy hosta nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="16117-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="16117-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="16117-120">This parameter is optional.</span></span>
<span data-ttu-id="16117-121">Jeśli nie określono, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="16117-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="16117-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="16117-122">-GatewayId</span></span>
<span data-ttu-id="16117-123">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="16117-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="16117-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="16117-124">This parameter is required.</span></span>

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

### <span data-ttu-id="16117-125">-Hostname (Nazwa hosta)</span><span class="sxs-lookup"><span data-stu-id="16117-125">-Hostname</span></span>
<span data-ttu-id="16117-126">Hostname (Nazwa hosta).</span><span class="sxs-lookup"><span data-stu-id="16117-126">Hostname.</span></span>
<span data-ttu-id="16117-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="16117-127">This parameter is required.</span></span>

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

### <span data-ttu-id="16117-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="16117-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="16117-129">Oflaguj, aby wymusić certyfikat NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="16117-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="16117-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="16117-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="16117-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16117-131">-Confirm</span></span>
<span data-ttu-id="16117-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="16117-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16117-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16117-133">-WhatIf</span></span>
<span data-ttu-id="16117-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16117-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16117-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="16117-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16117-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16117-136">CommonParameters</span></span>
<span data-ttu-id="16117-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16117-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16117-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16117-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16117-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16117-139">INPUTS</span></span>

### <span data-ttu-id="16117-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="16117-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="16117-141">System.String</span><span class="sxs-lookup"><span data-stu-id="16117-141">System.String</span></span>

### <span data-ttu-id="16117-142">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="16117-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="16117-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16117-143">OUTPUTS</span></span>

### <span data-ttu-id="16117-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="16117-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="16117-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="16117-145">NOTES</span></span>

## <span data-ttu-id="16117-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16117-146">RELATED LINKS</span></span>
