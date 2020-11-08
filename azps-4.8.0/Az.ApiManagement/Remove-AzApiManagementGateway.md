---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementGateway.md
ms.openlocfilehash: 9b6eac7a0c0c994797de51c936840da515ef3f4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063020"
---
# <span data-ttu-id="b3f65-101">Remove-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="b3f65-101">Remove-AzApiManagementGateway</span></span>

## <span data-ttu-id="b3f65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3f65-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f65-103">Odłączenie interfejsu API od bramy.</span><span class="sxs-lookup"><span data-stu-id="b3f65-103">Detaches an API from a Gateway.</span></span>

## <span data-ttu-id="b3f65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3f65-104">SYNTAX</span></span>

### <span data-ttu-id="b3f65-105">ContextParameterSetName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b3f65-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementGateway -Context <PsApiManagementContext> -GatewayId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3f65-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3f65-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementGateway -InputObject <PsApiManagementGateway> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3f65-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3f65-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementGateway -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3f65-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b3f65-108">DESCRIPTION</span></span>
<span data-ttu-id="b3f65-109">Polecenie cmdlet **Remove-AzApiManagementGateway** ODŁĄCZA interfejs API od bramy.</span><span class="sxs-lookup"><span data-stu-id="b3f65-109">The **Remove-AzApiManagementGateway** cmdlet detaches an API from a Gateway.</span></span>

## <span data-ttu-id="b3f65-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3f65-110">EXAMPLES</span></span>

### <span data-ttu-id="b3f65-111">Przykład 1. Usuń istniejącą bramę</span><span class="sxs-lookup"><span data-stu-id="b3f65-111">Example 1: Remove an existing gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementGateway -Context $apimContext -GatewayId "g0001" -Force
```

<span data-ttu-id="b3f65-112">To polecenie usuwa istniejącą bramę i nie monituje użytkownika o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b3f65-112">This command removes an existing gateway and does not prompt the user for confirmation.</span></span>

## <span data-ttu-id="b3f65-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3f65-113">PARAMETERS</span></span>

### <span data-ttu-id="b3f65-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b3f65-114">-Context</span></span>
<span data-ttu-id="b3f65-115">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b3f65-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b3f65-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b3f65-116">This parameter is required.</span></span>

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

### <span data-ttu-id="b3f65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f65-117">-DefaultProfile</span></span>
<span data-ttu-id="b3f65-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3f65-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b3f65-119">-GatewayId</span></span>
<span data-ttu-id="b3f65-120">Identyfikator istniejącej bramy.</span><span class="sxs-lookup"><span data-stu-id="b3f65-120">Identifier of existing gateway.</span></span>
<span data-ttu-id="b3f65-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b3f65-121">This parameter is required.</span></span>

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

### <span data-ttu-id="b3f65-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3f65-122">-InputObject</span></span>
<span data-ttu-id="b3f65-123">Wystąpienie PsApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="b3f65-123">Instance of PsApiManagementGateway.</span></span> <span data-ttu-id="b3f65-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b3f65-124">This parameter is required.</span></span>

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

### <span data-ttu-id="b3f65-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3f65-125">-PassThru</span></span>
<span data-ttu-id="b3f65-126">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="b3f65-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b3f65-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b3f65-127">This parameter is optional.</span></span>
<span data-ttu-id="b3f65-128">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="b3f65-128">Default value is false.</span></span>

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

### <span data-ttu-id="b3f65-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b3f65-129">-ResourceId</span></span>
<span data-ttu-id="b3f65-130">Identyfikator zasobu ARM bramy.</span><span class="sxs-lookup"><span data-stu-id="b3f65-130">Arm ResourceId of the Gateway.</span></span> <span data-ttu-id="b3f65-131">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b3f65-131">This parameter is required.</span></span>

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

### <span data-ttu-id="b3f65-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3f65-132">-Confirm</span></span>
<span data-ttu-id="b3f65-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3f65-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3f65-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3f65-134">-WhatIf</span></span>
<span data-ttu-id="b3f65-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3f65-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f65-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3f65-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3f65-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f65-137">CommonParameters</span></span>
<span data-ttu-id="b3f65-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3f65-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f65-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3f65-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f65-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3f65-140">INPUTS</span></span>

### <span data-ttu-id="b3f65-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b3f65-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b3f65-142">System. String</span><span class="sxs-lookup"><span data-stu-id="b3f65-142">System.String</span></span>

### <span data-ttu-id="b3f65-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b3f65-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b3f65-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3f65-144">OUTPUTS</span></span>

### <span data-ttu-id="b3f65-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3f65-145">System.Boolean</span></span>

## <span data-ttu-id="b3f65-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3f65-146">NOTES</span></span>

## <span data-ttu-id="b3f65-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3f65-147">RELATED LINKS</span></span>
