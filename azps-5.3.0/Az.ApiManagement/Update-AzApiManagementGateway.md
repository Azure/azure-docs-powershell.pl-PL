---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/Update-AzApiManagementGateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementGateway.md
ms.openlocfilehash: d053bc60390c43c3409bb7adfad5a3ff3720f5b7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381549"
---
# <span data-ttu-id="dba22-101">Update-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="dba22-101">Update-AzApiManagementGateway</span></span>

## <span data-ttu-id="dba22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dba22-102">SYNOPSIS</span></span>
<span data-ttu-id="dba22-103">Umożliwia skonfigurowanie bramy zarządzania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="dba22-103">Configures an API management Gateway.</span></span>

## <span data-ttu-id="dba22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dba22-104">SYNTAX</span></span>

### <span data-ttu-id="dba22-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dba22-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba22-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dba22-106">ByInputObject</span></span>
```
Update-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dba22-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dba22-107">ByResourceId</span></span>
```
Update-AzApiManagementGateway -ResourceId <String> [-Description <String>]
 [-LocationData <PsApiManagementResourceLocation>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba22-108">Opis</span><span class="sxs-lookup"><span data-stu-id="dba22-108">DESCRIPTION</span></span>
<span data-ttu-id="dba22-109">Polecenie cmdlet **Update-AzApiManagementGateway** konfiguruje bramę zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="dba22-109">The **Update-AzApiManagementGateway** cmdlet configures an API management Gateway.</span></span>

## <span data-ttu-id="dba22-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dba22-110">EXAMPLES</span></span>

### <span data-ttu-id="dba22-111">Przykład 1: Konfigurowanie grupy zarządzania</span><span class="sxs-lookup"><span data-stu-id="dba22-111">Example 1: Configure a management group</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementGateway -Context $apimContext -GatewayId "0001" -Description "Updated Gateway"
```

<span data-ttu-id="dba22-112">To polecenie umożliwia skonfigurowanie bramy.</span><span class="sxs-lookup"><span data-stu-id="dba22-112">This command configures a gateway.</span></span>

## <span data-ttu-id="dba22-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dba22-113">PARAMETERS</span></span>

### <span data-ttu-id="dba22-114">-Context</span><span class="sxs-lookup"><span data-stu-id="dba22-114">-Context</span></span>
<span data-ttu-id="dba22-115">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="dba22-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="dba22-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dba22-116">This parameter is required.</span></span>

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

### <span data-ttu-id="dba22-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba22-117">-DefaultProfile</span></span>
<span data-ttu-id="dba22-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dba22-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dba22-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="dba22-119">-Description</span></span>
<span data-ttu-id="dba22-120">Opis bramy.</span><span class="sxs-lookup"><span data-stu-id="dba22-120">Gateway description.</span></span>
<span data-ttu-id="dba22-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dba22-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="dba22-122">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="dba22-122">-GatewayId</span></span>
<span data-ttu-id="dba22-123">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="dba22-123">Identifier of existing gateway.</span></span>
<span data-ttu-id="dba22-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dba22-124">This parameter is required.</span></span>

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

### <span data-ttu-id="dba22-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dba22-125">-InputObject</span></span>
<span data-ttu-id="dba22-126">Wystąpienie PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="dba22-126">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="dba22-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dba22-127">This parameter is required.</span></span>

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

### <span data-ttu-id="dba22-128">-LocationData</span><span class="sxs-lookup"><span data-stu-id="dba22-128">-LocationData</span></span>
<span data-ttu-id="dba22-129">Lokalizacja bramy.</span><span class="sxs-lookup"><span data-stu-id="dba22-129">Gateway location.</span></span>
<span data-ttu-id="dba22-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dba22-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="dba22-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dba22-131">-PassThru</span></span>
<span data-ttu-id="dba22-132">W przypadku określenia wystąpienia funkcji Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementGateway (typ) reprezentujący zmodyfikowaną bramę.</span><span class="sxs-lookup"><span data-stu-id="dba22-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway type representing the modified gateway.</span></span>

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

### <span data-ttu-id="dba22-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dba22-133">-ResourceId</span></span>
<span data-ttu-id="dba22-134">Identyfikator zasobu ARM bramy.</span><span class="sxs-lookup"><span data-stu-id="dba22-134">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="dba22-135">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dba22-135">This parameter is required.</span></span>

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

### <span data-ttu-id="dba22-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dba22-136">-Confirm</span></span>
<span data-ttu-id="dba22-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dba22-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba22-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba22-138">-WhatIf</span></span>
<span data-ttu-id="dba22-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dba22-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba22-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dba22-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba22-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba22-141">CommonParameters</span></span>
<span data-ttu-id="dba22-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba22-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba22-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dba22-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba22-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dba22-144">INPUTS</span></span>

### <span data-ttu-id="dba22-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dba22-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dba22-146">System. String</span><span class="sxs-lookup"><span data-stu-id="dba22-146">System.String</span></span>

### <span data-ttu-id="dba22-147">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="dba22-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

### <span data-ttu-id="dba22-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dba22-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dba22-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dba22-149">OUTPUTS</span></span>

### <span data-ttu-id="dba22-150">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="dba22-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="dba22-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dba22-151">NOTES</span></span>

## <span data-ttu-id="dba22-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dba22-152">RELATED LINKS</span></span>
