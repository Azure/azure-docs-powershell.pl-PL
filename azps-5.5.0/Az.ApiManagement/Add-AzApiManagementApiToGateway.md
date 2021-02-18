---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239922"
---
# <span data-ttu-id="418af-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="418af-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="418af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="418af-102">SYNOPSIS</span></span>
<span data-ttu-id="418af-103">Dołącza interfejs API do bramy.</span><span class="sxs-lookup"><span data-stu-id="418af-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="418af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="418af-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="418af-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="418af-105">DESCRIPTION</span></span>
<span data-ttu-id="418af-106">Polecenie **cmdlet Add-AzApiManagementApiToGateway** dodaje interfejs API zarządzania interfejsem Azure API do bramy.</span><span class="sxs-lookup"><span data-stu-id="418af-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="418af-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="418af-107">EXAMPLES</span></span>

### <span data-ttu-id="418af-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="418af-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="418af-109">To polecenie dodaje określony interfejs API do określonej bramy.</span><span class="sxs-lookup"><span data-stu-id="418af-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="418af-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="418af-110">PARAMETERS</span></span>

### <span data-ttu-id="418af-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="418af-111">-ApiId</span></span>
<span data-ttu-id="418af-112">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="418af-112">Identifier of existing API.</span></span>
<span data-ttu-id="418af-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="418af-113">This parameter is required.</span></span>

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

### <span data-ttu-id="418af-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="418af-114">-Context</span></span>
<span data-ttu-id="418af-115">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="418af-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="418af-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="418af-116">This parameter is required.</span></span>

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

### <span data-ttu-id="418af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="418af-117">-DefaultProfile</span></span>
<span data-ttu-id="418af-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="418af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="418af-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="418af-119">-GatewayId</span></span>
<span data-ttu-id="418af-120">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="418af-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="418af-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="418af-121">This parameter is required.</span></span>

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

### <span data-ttu-id="418af-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="418af-122">-PassThru</span></span>
<span data-ttu-id="418af-123">Jeśli zostanie określona, na wypadek, gdyby operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="418af-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="418af-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="418af-124">This parameter is optional.</span></span>
<span data-ttu-id="418af-125">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="418af-125">Default value is false.</span></span>

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

### <span data-ttu-id="418af-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="418af-126">-ProvisioningState</span></span>
<span data-ttu-id="418af-127">Stan inicjowania obsługi administracyjnej (utworzono).</span><span class="sxs-lookup"><span data-stu-id="418af-127">Provisioning State (Created).</span></span>
<span data-ttu-id="418af-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="418af-128">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState]
Parameter Sets: (All)
Aliases:
Accepted values: Created

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="418af-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="418af-129">-Confirm</span></span>
<span data-ttu-id="418af-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="418af-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="418af-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="418af-131">-WhatIf</span></span>
<span data-ttu-id="418af-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="418af-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="418af-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="418af-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="418af-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="418af-134">CommonParameters</span></span>
<span data-ttu-id="418af-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="418af-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="418af-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="418af-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="418af-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="418af-137">INPUTS</span></span>

### <span data-ttu-id="418af-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="418af-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="418af-139">System.String</span><span class="sxs-lookup"><span data-stu-id="418af-139">System.String</span></span>

### <span data-ttu-id="418af-140">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlet.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="418af-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="418af-141">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="418af-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="418af-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="418af-142">OUTPUTS</span></span>

### <span data-ttu-id="418af-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="418af-143">System.Boolean</span></span>

## <span data-ttu-id="418af-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="418af-144">NOTES</span></span>

## <span data-ttu-id="418af-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="418af-145">RELATED LINKS</span></span>

[<span data-ttu-id="418af-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="418af-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)