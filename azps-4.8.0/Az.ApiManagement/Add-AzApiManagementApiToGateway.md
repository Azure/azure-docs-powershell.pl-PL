---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064598"
---
# <span data-ttu-id="e8f16-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="e8f16-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="e8f16-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8f16-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f16-103">Dołącza interfejs API do bramy.</span><span class="sxs-lookup"><span data-stu-id="e8f16-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="e8f16-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8f16-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8f16-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8f16-105">DESCRIPTION</span></span>
<span data-ttu-id="e8f16-106">Polecenie cmdlet **Add-AzApiManagementApiToGateway** umożliwia dodanie interfejsu API zarządzania interfejsem Azure API do bramy.</span><span class="sxs-lookup"><span data-stu-id="e8f16-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="e8f16-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8f16-107">EXAMPLES</span></span>

### <span data-ttu-id="e8f16-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e8f16-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="e8f16-109">To polecenie umożliwia dodanie określonego interfejsu API do określonej bramy.</span><span class="sxs-lookup"><span data-stu-id="e8f16-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="e8f16-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8f16-110">PARAMETERS</span></span>

### <span data-ttu-id="e8f16-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e8f16-111">-ApiId</span></span>
<span data-ttu-id="e8f16-112">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="e8f16-112">Identifier of existing API.</span></span>
<span data-ttu-id="e8f16-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e8f16-113">This parameter is required.</span></span>

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

### <span data-ttu-id="e8f16-114">-Context</span><span class="sxs-lookup"><span data-stu-id="e8f16-114">-Context</span></span>
<span data-ttu-id="e8f16-115">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e8f16-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e8f16-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e8f16-116">This parameter is required.</span></span>

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

### <span data-ttu-id="e8f16-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f16-117">-DefaultProfile</span></span>
<span data-ttu-id="e8f16-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f16-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8f16-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="e8f16-119">-GatewayId</span></span>
<span data-ttu-id="e8f16-120">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="e8f16-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="e8f16-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e8f16-121">This parameter is required.</span></span>

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

### <span data-ttu-id="e8f16-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8f16-122">-PassThru</span></span>
<span data-ttu-id="e8f16-123">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="e8f16-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e8f16-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8f16-124">This parameter is optional.</span></span>
<span data-ttu-id="e8f16-125">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="e8f16-125">Default value is false.</span></span>

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

### <span data-ttu-id="e8f16-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="e8f16-126">-ProvisioningState</span></span>
<span data-ttu-id="e8f16-127">Stan inicjowania obsługi (utworzony).</span><span class="sxs-lookup"><span data-stu-id="e8f16-127">Provisioning State (Created).</span></span>
<span data-ttu-id="e8f16-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8f16-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8f16-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8f16-129">-Confirm</span></span>
<span data-ttu-id="e8f16-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8f16-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f16-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f16-131">-WhatIf</span></span>
<span data-ttu-id="e8f16-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8f16-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8f16-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8f16-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f16-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f16-134">CommonParameters</span></span>
<span data-ttu-id="e8f16-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8f16-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f16-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e8f16-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f16-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8f16-137">INPUTS</span></span>

### <span data-ttu-id="e8f16-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e8f16-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8f16-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f16-139">System.String</span></span>

### <span data-ttu-id="e8f16-140">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementGatewayApiProvisioningState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e8f16-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e8f16-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e8f16-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e8f16-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8f16-142">OUTPUTS</span></span>

### <span data-ttu-id="e8f16-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e8f16-143">System.Boolean</span></span>

## <span data-ttu-id="e8f16-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8f16-144">NOTES</span></span>

## <span data-ttu-id="e8f16-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8f16-145">RELATED LINKS</span></span>

[<span data-ttu-id="e8f16-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="e8f16-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)