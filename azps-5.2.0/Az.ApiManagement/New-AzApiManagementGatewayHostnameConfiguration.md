---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: 6aadf94ff379df322907be66c73052196de803c5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356503"
---
# <span data-ttu-id="338ab-101">New-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="338ab-101">New-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="338ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="338ab-102">SYNOPSIS</span></span>
<span data-ttu-id="338ab-103">Tworzy nazwę hosta configuratin dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="338ab-103">Creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="338ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="338ab-104">SYNTAX</span></span>

```
New-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 [-GatewayHostnameConfigurationId <String>] -Hostname <String> -CertificateResourceId <String>
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="338ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="338ab-105">DESCRIPTION</span></span>
<span data-ttu-id="338ab-106">Polecenie cmdlet **New-AzApiManagementGatewayHostnameConfiguration** tworzy nazwę hosta configuratin dla istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="338ab-106">The **New-AzApiManagementGatewayHostnameConfiguration** cmdlet creates a hostname configuratin for the existing Gateway.</span></span>

## <span data-ttu-id="338ab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="338ab-107">EXAMPLES</span></span>

### <span data-ttu-id="338ab-108">Przykład 1. Tworzenie konfiguracji nazwy hosta dla istniejącej bramy</span><span class="sxs-lookup"><span data-stu-id="338ab-108">Example 1: Create a hostname configuration for the existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$cert = Get-AzApiManagementCertificate -Context $apimContext -CertificateId "333"
PS C:\>New-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g01" -GatewayHostnameConfigurationId "h01" -Hostname "www.contoso.com" -CertificateResourceId $cert.Id
```

<span data-ttu-id="338ab-109">To polecenie tworzy konfigurację hosta "H01" dla bramy "G01".</span><span class="sxs-lookup"><span data-stu-id="338ab-109">This command creates a "h01" hostname configuration for a "g01" gateway.</span></span>

## <span data-ttu-id="338ab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="338ab-110">PARAMETERS</span></span>

### <span data-ttu-id="338ab-111">-CertificateResourceId</span><span class="sxs-lookup"><span data-stu-id="338ab-111">-CertificateResourceId</span></span>
<span data-ttu-id="338ab-112">Identyfikator zasobu dla istniejącego identyfikatora certyfikatu. Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="338ab-112">A resource identifier for the existing certificate id. This parameter is required.</span></span>

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

### <span data-ttu-id="338ab-113">-Context</span><span class="sxs-lookup"><span data-stu-id="338ab-113">-Context</span></span>
<span data-ttu-id="338ab-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="338ab-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="338ab-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="338ab-115">This parameter is required.</span></span>

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

### <span data-ttu-id="338ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="338ab-116">-DefaultProfile</span></span>
<span data-ttu-id="338ab-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="338ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="338ab-118">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="338ab-118">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="338ab-119">Identyfikator nowej nazwy hosta bramy confiuration.</span><span class="sxs-lookup"><span data-stu-id="338ab-119">Identifier of new gateway hostname confiuration.</span></span>
<span data-ttu-id="338ab-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="338ab-120">This parameter is optional.</span></span>
<span data-ttu-id="338ab-121">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="338ab-121">If not specified will be generated.</span></span>

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

### <span data-ttu-id="338ab-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="338ab-122">-GatewayId</span></span>
<span data-ttu-id="338ab-123">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="338ab-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="338ab-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="338ab-124">This parameter is required.</span></span>

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

### <span data-ttu-id="338ab-125">-Hostname</span><span class="sxs-lookup"><span data-stu-id="338ab-125">-Hostname</span></span>
<span data-ttu-id="338ab-126">Nazwą.</span><span class="sxs-lookup"><span data-stu-id="338ab-126">Hostname.</span></span>
<span data-ttu-id="338ab-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="338ab-127">This parameter is required.</span></span>

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

### <span data-ttu-id="338ab-128">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="338ab-128">-NegotiateClientCertificate</span></span>
<span data-ttu-id="338ab-129">Flaga wymuszania NegotiateClientCertificate.</span><span class="sxs-lookup"><span data-stu-id="338ab-129">Flag to enforce NegotiateClientCertificate.</span></span>
<span data-ttu-id="338ab-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="338ab-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="338ab-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="338ab-131">-Confirm</span></span>
<span data-ttu-id="338ab-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="338ab-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="338ab-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="338ab-133">-WhatIf</span></span>
<span data-ttu-id="338ab-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="338ab-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="338ab-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="338ab-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="338ab-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338ab-136">CommonParameters</span></span>
<span data-ttu-id="338ab-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="338ab-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338ab-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="338ab-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338ab-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="338ab-139">INPUTS</span></span>

### <span data-ttu-id="338ab-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="338ab-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="338ab-141">System. String</span><span class="sxs-lookup"><span data-stu-id="338ab-141">System.String</span></span>

### <span data-ttu-id="338ab-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="338ab-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="338ab-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="338ab-143">OUTPUTS</span></span>

### <span data-ttu-id="338ab-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="338ab-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="338ab-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="338ab-145">NOTES</span></span>

## <span data-ttu-id="338ab-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="338ab-146">RELATED LINKS</span></span>
