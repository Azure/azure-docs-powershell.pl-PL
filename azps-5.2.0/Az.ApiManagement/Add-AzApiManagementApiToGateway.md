---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitogateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToGateway.md
ms.openlocfilehash: 6bb40d46c80e609824b1c56d05091ade5716f7f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345445"
---
# <span data-ttu-id="c3197-101">Add-AzApiManagementApiToGateway</span><span class="sxs-lookup"><span data-stu-id="c3197-101">Add-AzApiManagementApiToGateway</span></span>

## <span data-ttu-id="c3197-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3197-102">SYNOPSIS</span></span>
<span data-ttu-id="c3197-103">Dołącza interfejs API do bramy.</span><span class="sxs-lookup"><span data-stu-id="c3197-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="c3197-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3197-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-ProvisioningState <PsApiManagementGatewayApiProvisioningState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3197-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c3197-105">DESCRIPTION</span></span>
<span data-ttu-id="c3197-106">Polecenie cmdlet **Add-AzApiManagementApiToGateway** umożliwia dodanie interfejsu API zarządzania interfejsem Azure API do bramy.</span><span class="sxs-lookup"><span data-stu-id="c3197-106">The **Add-AzApiManagementApiToGateway** cmdlet adds an Azure API Management API to a Gateway.</span></span>

## <span data-ttu-id="c3197-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3197-107">EXAMPLES</span></span>

### <span data-ttu-id="c3197-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3197-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001"
```

<span data-ttu-id="c3197-109">To polecenie umożliwia dodanie określonego interfejsu API do określonej bramy.</span><span class="sxs-lookup"><span data-stu-id="c3197-109">This command adds the specified API to the specified Gateway.</span></span>

## <span data-ttu-id="c3197-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3197-110">PARAMETERS</span></span>

### <span data-ttu-id="c3197-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c3197-111">-ApiId</span></span>
<span data-ttu-id="c3197-112">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c3197-112">Identifier of existing API.</span></span>
<span data-ttu-id="c3197-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c3197-113">This parameter is required.</span></span>

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

### <span data-ttu-id="c3197-114">-Context</span><span class="sxs-lookup"><span data-stu-id="c3197-114">-Context</span></span>
<span data-ttu-id="c3197-115">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c3197-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c3197-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c3197-116">This parameter is required.</span></span>

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

### <span data-ttu-id="c3197-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3197-117">-DefaultProfile</span></span>
<span data-ttu-id="c3197-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3197-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3197-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="c3197-119">-GatewayId</span></span>
<span data-ttu-id="c3197-120">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="c3197-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="c3197-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c3197-121">This parameter is required.</span></span>

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

### <span data-ttu-id="c3197-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3197-122">-PassThru</span></span>
<span data-ttu-id="c3197-123">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="c3197-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c3197-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c3197-124">This parameter is optional.</span></span>
<span data-ttu-id="c3197-125">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="c3197-125">Default value is false.</span></span>

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

### <span data-ttu-id="c3197-126">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="c3197-126">-ProvisioningState</span></span>
<span data-ttu-id="c3197-127">Stan inicjowania obsługi (utworzony).</span><span class="sxs-lookup"><span data-stu-id="c3197-127">Provisioning State (Created).</span></span>
<span data-ttu-id="c3197-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c3197-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="c3197-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3197-129">-Confirm</span></span>
<span data-ttu-id="c3197-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3197-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3197-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3197-131">-WhatIf</span></span>
<span data-ttu-id="c3197-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3197-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3197-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3197-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3197-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3197-134">CommonParameters</span></span>
<span data-ttu-id="c3197-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3197-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3197-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c3197-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3197-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3197-137">INPUTS</span></span>

### <span data-ttu-id="c3197-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c3197-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c3197-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c3197-139">System.String</span></span>

### <span data-ttu-id="c3197-140">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementGatewayApiProvisioningState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 2.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c3197-140">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGatewayApiProvisioningState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c3197-141">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c3197-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c3197-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3197-142">OUTPUTS</span></span>

### <span data-ttu-id="c3197-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3197-143">System.Boolean</span></span>

## <span data-ttu-id="c3197-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3197-144">NOTES</span></span>

## <span data-ttu-id="c3197-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3197-145">RELATED LINKS</span></span>

[<span data-ttu-id="c3197-146">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="c3197-146">Remove-AzApiManagementApiFromGateway</span></span>](./Remove-AzApiManagementApiFromGateway.md)