---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: 62131f634d049afe137b635d6a970d37e2173b8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001930"
---
# <span data-ttu-id="dae2f-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="dae2f-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="dae2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dae2f-102">SYNOPSIS</span></span>
<span data-ttu-id="dae2f-103">Konfiguruje bramę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="dae2f-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="dae2f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dae2f-104">SYNTAX</span></span>

### <span data-ttu-id="dae2f-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dae2f-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae2f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dae2f-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dae2f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dae2f-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dae2f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="dae2f-108">DESCRIPTION</span></span>
<span data-ttu-id="dae2f-109">Polecenie **cmdlet Update-AzApiManagementGateway** konfiguruje bramę zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="dae2f-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="dae2f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dae2f-110">EXAMPLES</span></span>

### <span data-ttu-id="dae2f-111">Przykład 1. Konfigurowanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="dae2f-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="dae2f-112">To polecenie konfiguruje bramę.</span><span class="sxs-lookup"><span data-stu-id="dae2f-112">This command configures a gateway.</span></span>

## <span data-ttu-id="dae2f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dae2f-113">PARAMETERS</span></span>

### <span data-ttu-id="dae2f-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="dae2f-114">-Context</span></span>
<span data-ttu-id="dae2f-115">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dae2f-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dae2f-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dae2f-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dae2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dae2f-117">-DefaultProfile</span></span>
<span data-ttu-id="dae2f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dae2f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dae2f-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="dae2f-119">-Description</span></span>
<span data-ttu-id="dae2f-120">Opis bramy.</span><span class="sxs-lookup"><span data-stu-id="dae2f-120">Gateway description.</span></span>
<span data-ttu-id="dae2f-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dae2f-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="dae2f-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="dae2f-122">-GatewayId</span></span>
<span data-ttu-id="dae2f-123">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="dae2f-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="dae2f-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dae2f-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae2f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dae2f-125">-InputObject</span></span>
<span data-ttu-id="dae2f-126">Wystąpienie aplikacji PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="dae2f-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="dae2f-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dae2f-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dae2f-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="dae2f-128">-LocationData</span></span>
<span data-ttu-id="dae2f-129">Lokalizacja bramy.</span><span class="sxs-lookup"><span data-stu-id="dae2f-129">Gateway location.</span></span>
<span data-ttu-id="dae2f-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dae2f-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae2f-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dae2f-131">-PassThru</span></span>
<span data-ttu-id="dae2f-132">Jeśli określono, wówczas wystąpienie właściwości Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway typ reprezentujący zmodyfikowaną bramę.</span><span class="sxs-lookup"><span data-stu-id="dae2f-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="dae2f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dae2f-133">-ResourceId</span></span>
<span data-ttu-id="dae2f-134">Arm ResourceId bramy.</span><span class="sxs-lookup"><span data-stu-id="dae2f-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="dae2f-135">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dae2f-135">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dae2f-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dae2f-136">-Confirm</span></span>
<span data-ttu-id="dae2f-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dae2f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dae2f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dae2f-138">-WhatIf</span></span>
<span data-ttu-id="dae2f-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dae2f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dae2f-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dae2f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dae2f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dae2f-141">CommonParameters</span></span>
<span data-ttu-id="dae2f-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dae2f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dae2f-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dae2f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dae2f-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dae2f-144">INPUTS</span></span>

### <span data-ttu-id="dae2f-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dae2f-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dae2f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="dae2f-146">System.String</span></span>

### <span data-ttu-id="dae2f-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="dae2f-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="dae2f-148">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="dae2f-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dae2f-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dae2f-149">OUTPUTS</span></span>

### <span data-ttu-id="dae2f-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="dae2f-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="dae2f-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dae2f-151">NOTES</span></span>

## <span data-ttu-id="dae2f-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dae2f-152">RELATED LINKS</span></span>
