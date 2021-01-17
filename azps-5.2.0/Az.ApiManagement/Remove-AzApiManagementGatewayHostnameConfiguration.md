---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgatewayhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGatewayHostnameConfiguration.md
ms.openlocfilehash: e1999387cc2beb5a55fba3aef771a76440804f22
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98361398"
---
# <span data-ttu-id="4dd11-101">Remove-AzApiManagementGatewayHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4dd11-101">Remove-AzApiManagementGatewayHostnameConfiguration</span></span>

## <span data-ttu-id="4dd11-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4dd11-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd11-103">Usuwa konfigurację hosta z istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="4dd11-103">Removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="4dd11-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4dd11-104">SYNTAX</span></span>

### <span data-ttu-id="4dd11-105">ContextParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4dd11-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -Context <PsApiManagementContext> -GatewayId <String>
 -GatewayHostnameConfigurationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd11-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd11-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -InputObject <PsApiManagementGatewayHostnameConfiguration>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dd11-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dd11-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGatewayHostnameConfiguration -ResourceId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd11-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4dd11-108">DESCRIPTION</span></span>
<span data-ttu-id="4dd11-109">Polecenie cmdlet **Remove-AzApiManagementGatewayHostnameConfiguration** usuwa konfigurację hosta z istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="4dd11-109">The **Remove-AzApiManagementGatewayHostnameConfiguration** cmdlet removes a hostname configuration from the existing Gateway.</span></span>

## <span data-ttu-id="4dd11-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4dd11-110">EXAMPLES</span></span>

### <span data-ttu-id="4dd11-111">Przykład 1: usuwanie istniejącej konfiguracji nazwy hosta bramy</span><span class="sxs-lookup"><span data-stu-id="4dd11-111">Example 1: Remove an existing gateway hostname configuration</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGatewayHostnameConfiguration -Context $apimContext -GatewayId "g0001" -GatewayHostnameConfigurationId "h0001" -Force
```

<span data-ttu-id="4dd11-112">To polecenie usuwa istniejącą konfigurację hosta bramy i nie monituje użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4dd11-112">This command removes an existing gateway hostname configuration and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="4dd11-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4dd11-113">PARAMETERS</span></span>

### <span data-ttu-id="4dd11-114">-Context</span><span class="sxs-lookup"><span data-stu-id="4dd11-114">-Context</span></span>
<span data-ttu-id="4dd11-115">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4dd11-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4dd11-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4dd11-116">This parameter is required.</span></span>

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

### <span data-ttu-id="4dd11-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd11-117">-DefaultProfile</span></span>
<span data-ttu-id="4dd11-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd11-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dd11-119">-GatewayHostnameConfigurationId</span><span class="sxs-lookup"><span data-stu-id="4dd11-119">-GatewayHostnameConfigurationId</span></span>
<span data-ttu-id="4dd11-120">Identyfikator istniejącej konfiguracji hosta bramy.</span><span class="sxs-lookup"><span data-stu-id="4dd11-120">Identifier of existing gateway hostname configuration.</span></span>
<span data-ttu-id="4dd11-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4dd11-121">This parameter is required.</span></span>

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

### <span data-ttu-id="4dd11-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="4dd11-122">-GatewayId</span></span>
<span data-ttu-id="4dd11-123">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="4dd11-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="4dd11-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4dd11-124">This parameter is required.</span></span>

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

### <span data-ttu-id="4dd11-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4dd11-125">-InputObject</span></span>
<span data-ttu-id="4dd11-126">Wystąpienie PsApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4dd11-126">Instance of PsApiManagementGatewayHostnameConfiguration.</span></span> <span data-ttu-id="4dd11-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4dd11-127">This parameter is required.</span></span>

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

### <span data-ttu-id="4dd11-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dd11-128">-PassThru</span></span>
<span data-ttu-id="4dd11-129">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="4dd11-129">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4dd11-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="4dd11-130">This parameter is optional.</span></span>
<span data-ttu-id="4dd11-131">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="4dd11-131">Default value is false.</span></span>

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

### <span data-ttu-id="4dd11-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dd11-132">-ResourceId</span></span>
<span data-ttu-id="4dd11-133">Identyfikator zasobu ARM GatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4dd11-133">Arm ResourceId of the GatewayHostnameConfiguration.</span></span> <span data-ttu-id="4dd11-134">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4dd11-134">This parameter is required.</span></span>

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

### <span data-ttu-id="4dd11-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4dd11-135">-Confirm</span></span>
<span data-ttu-id="4dd11-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd11-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dd11-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd11-137">-WhatIf</span></span>
<span data-ttu-id="4dd11-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dd11-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd11-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4dd11-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dd11-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd11-140">CommonParameters</span></span>
<span data-ttu-id="4dd11-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dd11-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd11-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dd11-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd11-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4dd11-143">INPUTS</span></span>

### <span data-ttu-id="4dd11-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4dd11-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4dd11-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4dd11-145">System.String</span></span>

### <span data-ttu-id="4dd11-146">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4dd11-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4dd11-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4dd11-147">OUTPUTS</span></span>

### <span data-ttu-id="4dd11-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4dd11-148">System.Boolean</span></span>

## <span data-ttu-id="4dd11-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4dd11-149">NOTES</span></span>

## <span data-ttu-id="4dd11-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4dd11-150">RELATED LINKS</span></span>
