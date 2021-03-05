---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 2ccd68fb5c1028408771e3011642797c8125ace3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994526"
---
# <span data-ttu-id="e690a-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="e690a-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="e690a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e690a-102">SYNOPSIS</span></span>
<span data-ttu-id="e690a-103">Odłącza interfejs API od bramy.</span><span class="sxs-lookup"><span data-stu-id="e690a-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="e690a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e690a-104">SYNTAX</span></span>

### <span data-ttu-id="e690a-105">ContextParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="e690a-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e690a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e690a-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e690a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e690a-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e690a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e690a-108">DESCRIPTION</span></span>
<span data-ttu-id="e690a-109">Polecenie **cmdlet Remove-AzApiManagementGateway** odłącza interfejs API od bramy.</span><span class="sxs-lookup"><span data-stu-id="e690a-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="e690a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e690a-110">EXAMPLES</span></span>

### <span data-ttu-id="e690a-111">Przykład 1. Usuwanie istniejącej bramy</span><span class="sxs-lookup"><span data-stu-id="e690a-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="e690a-112">To polecenie usuwa istniejącą bramę i nie monituje użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e690a-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="e690a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e690a-113">PARAMETERS</span></span>

### <span data-ttu-id="e690a-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e690a-114">-Context</span></span>
<span data-ttu-id="e690a-115">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e690a-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e690a-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e690a-116">This parameter is required.</span></span>

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

### <span data-ttu-id="e690a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e690a-117">-DefaultProfile</span></span>
<span data-ttu-id="e690a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e690a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e690a-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e690a-119">-GatewayId</span></span>
<span data-ttu-id="e690a-120">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="e690a-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="e690a-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e690a-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e690a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e690a-122">-InputObject</span></span>
<span data-ttu-id="e690a-123">Wystąpienie aplikacji PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="e690a-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="e690a-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e690a-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e690a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e690a-125">-PassThru</span></span>
<span data-ttu-id="e690a-126">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="e690a-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e690a-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e690a-127">This parameter is optional.</span></span>
<span data-ttu-id="e690a-128">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="e690a-128">Default value is false.</span></span>

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

### <span data-ttu-id="e690a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e690a-129">-ResourceId</span></span>
<span data-ttu-id="e690a-130">Arm ResourceId bramy.</span><span class="sxs-lookup"><span data-stu-id="e690a-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="e690a-131">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e690a-131">This parameter is required.</span></span>

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

### <span data-ttu-id="e690a-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e690a-132">-Confirm</span></span>
<span data-ttu-id="e690a-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e690a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e690a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e690a-134">-WhatIf</span></span>
<span data-ttu-id="e690a-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e690a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e690a-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e690a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e690a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e690a-137">CommonParameters</span></span>
<span data-ttu-id="e690a-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e690a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e690a-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e690a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e690a-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e690a-140">INPUTS</span></span>

### <span data-ttu-id="e690a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e690a-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e690a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e690a-142">System.String</span></span>

### <span data-ttu-id="e690a-143">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e690a-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e690a-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e690a-144">OUTPUTS</span></span>

### <span data-ttu-id="e690a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e690a-145">System.Boolean</span></span>

## <span data-ttu-id="e690a-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e690a-146">NOTES</span></span>

## <span data-ttu-id="e690a-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e690a-147">RELATED LINKS</span></span>
