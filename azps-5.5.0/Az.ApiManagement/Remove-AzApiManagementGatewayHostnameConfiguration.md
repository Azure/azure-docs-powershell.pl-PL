---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178043"
---
# <span data-ttu-id="88d75-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="88d75-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="88d75-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88d75-102">SYNOPSIS</span></span>
<span data-ttu-id="88d75-103">Usuwa konfigurację nazwy hosta z istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="88d75-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="88d75-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88d75-104">SYNTAX</span></span>

### <span data-ttu-id="88d75-105">ContextParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="88d75-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88d75-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88d75-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88d75-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88d75-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88d75-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="88d75-108">DESCRIPTION</span></span>
<span data-ttu-id="88d75-109">Polecenie **cmdlet Remove-AzApiManagementGatewayHostnameConfiguration** usuwa konfigurację nazwy hosta z istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="88d75-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="88d75-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88d75-110">EXAMPLES</span></span>

### <span data-ttu-id="88d75-111">Przykład 1. Usuwanie istniejącej konfiguracji nazwy hosta bramy</span><span class="sxs-lookup"><span data-stu-id="88d75-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="88d75-112">To polecenie usuwa istniejącą konfigurację nazwy hosta bramy i nie monituje użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88d75-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="88d75-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88d75-113">PARAMETERS</span></span>

### <span data-ttu-id="88d75-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="88d75-114">-Context</span></span>
<span data-ttu-id="88d75-115">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="88d75-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="88d75-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="88d75-116">This parameter is required.</span></span>

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

### <span data-ttu-id="88d75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88d75-117">-DefaultProfile</span></span>
<span data-ttu-id="88d75-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="88d75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88d75-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="88d75-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="88d75-120">Identyfikator istniejącej konfiguracji nazwy hosta bramy.</span><span class="sxs-lookup"><span data-stu-id="88d75-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="88d75-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="88d75-121">This parameter is required.</span></span>

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

### <span data-ttu-id="88d75-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="88d75-122">-GatewayId</span></span>
<span data-ttu-id="88d75-123">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="88d75-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="88d75-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="88d75-124">This parameter is required.</span></span>

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

### <span data-ttu-id="88d75-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="88d75-125">-InputObject</span></span>
<span data-ttu-id="88d75-126">Wystąpienie parametru PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="88d75-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="88d75-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="88d75-127">This parameter is required.</span></span>

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

### <span data-ttu-id="88d75-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88d75-128">-PassThru</span></span>
<span data-ttu-id="88d75-129">Jeśli zostanie określona, na wypadek, gdyby operacja zakończyła się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="88d75-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="88d75-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="88d75-130">This parameter is optional.</span></span>
<span data-ttu-id="88d75-131">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="88d75-131">Default value is false.</span></span>

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

### <span data-ttu-id="88d75-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88d75-132">-ResourceId</span></span>
<span data-ttu-id="88d75-133">Arm ResourceId (Adres Zasobu Arm) parametru GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="88d75-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="88d75-134">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="88d75-134">This parameter is required.</span></span>

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

### <span data-ttu-id="88d75-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88d75-135">-Confirm</span></span>
<span data-ttu-id="88d75-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88d75-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88d75-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88d75-137">-WhatIf</span></span>
<span data-ttu-id="88d75-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88d75-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88d75-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="88d75-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88d75-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88d75-140">CommonParameters</span></span>
<span data-ttu-id="88d75-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88d75-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88d75-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88d75-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88d75-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88d75-143">INPUTS</span></span>

### <span data-ttu-id="88d75-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="88d75-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="88d75-145">System.String</span><span class="sxs-lookup"><span data-stu-id="88d75-145">System.String</span></span>

### <span data-ttu-id="88d75-146">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="88d75-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="88d75-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88d75-147">OUTPUTS</span></span>

### <span data-ttu-id="88d75-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88d75-148">System.Boolean</span></span>

## <span data-ttu-id="88d75-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88d75-149">NOTES</span></span>

## <span data-ttu-id="88d75-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88d75-150">RELATED LINKS</span></span>
