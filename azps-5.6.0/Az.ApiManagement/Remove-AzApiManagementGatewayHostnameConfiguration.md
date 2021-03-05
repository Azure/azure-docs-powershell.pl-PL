---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: ad0c40e649384d4fb2bef9220f6ab8a994dea96c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012842"
---
# <span data-ttu-id="9059a-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="9059a-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="9059a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9059a-102">SYNOPSIS</span></span>
<span data-ttu-id="9059a-103">Usuwa konfigurację nazwy hosta z istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="9059a-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="9059a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9059a-104">SYNTAX</span></span>

### <span data-ttu-id="9059a-105">ContextParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="9059a-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9059a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9059a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9059a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9059a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9059a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9059a-108">DESCRIPTION</span></span>
<span data-ttu-id="9059a-109">Polecenie **cmdlet Remove-AzApiManagementGatewayHostnameConfiguration** usuwa konfigurację nazwy hosta z istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="9059a-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="9059a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9059a-110">EXAMPLES</span></span>

### <span data-ttu-id="9059a-111">Przykład 1. Usuwanie istniejącej konfiguracji nazwy hosta bramy</span><span class="sxs-lookup"><span data-stu-id="9059a-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="9059a-112">To polecenie usuwa istniejącą konfigurację nazwy hosta bramy i nie monituje użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9059a-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="9059a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9059a-113">PARAMETERS</span></span>

### <span data-ttu-id="9059a-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9059a-114">-Context</span></span>
<span data-ttu-id="9059a-115">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9059a-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9059a-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9059a-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9059a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9059a-117">-DefaultProfile</span></span>
<span data-ttu-id="9059a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9059a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9059a-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="9059a-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="9059a-120">Identyfikator istniejącej konfiguracji nazwy hosta bramy.</span><span class="sxs-lookup"><span data-stu-id="9059a-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="9059a-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9059a-121">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9059a-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="9059a-122">-GatewayId</span></span>
<span data-ttu-id="9059a-123">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="9059a-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="9059a-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9059a-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9059a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9059a-125">-InputObject</span></span>
<span data-ttu-id="9059a-126">Wystąpienie parametru PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9059a-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="9059a-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9059a-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayHostnameConfiguration
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9059a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9059a-128">-PassThru</span></span>
<span data-ttu-id="9059a-129">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9059a-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="9059a-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9059a-130">This parameter is optional.</span></span>
<span data-ttu-id="9059a-131">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="9059a-131">Default value is false.</span></span>

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

### <span data-ttu-id="9059a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9059a-132">-ResourceId</span></span>
<span data-ttu-id="9059a-133">Adres Arm ResourceId parametru GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="9059a-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="9059a-134">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9059a-134">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9059a-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9059a-135">-Confirm</span></span>
<span data-ttu-id="9059a-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9059a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9059a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9059a-137">-WhatIf</span></span>
<span data-ttu-id="9059a-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9059a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9059a-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9059a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9059a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9059a-140">CommonParameters</span></span>
<span data-ttu-id="9059a-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9059a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9059a-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9059a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9059a-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9059a-143">INPUTS</span></span>

### <span data-ttu-id="9059a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9059a-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9059a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="9059a-145">System.String</span></span>

### <span data-ttu-id="9059a-146">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="9059a-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9059a-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9059a-147">OUTPUTS</span></span>

### <span data-ttu-id="9059a-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9059a-148">System.Boolean</span></span>

## <span data-ttu-id="9059a-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9059a-149">NOTES</span></span>

## <span data-ttu-id="9059a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9059a-150">RELATED LINKS</span></span>
