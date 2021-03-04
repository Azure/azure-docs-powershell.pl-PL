---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 2b50ddb0186e1c7ca8bc0da237f3fca833cb7367
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959073"
---
# <span data-ttu-id="7915a-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="7915a-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="7915a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7915a-102">SYNOPSIS</span></span>
<span data-ttu-id="7915a-103">Dołącza interfejs API do bramy.</span><span class="sxs-lookup"><span data-stu-id="7915a-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="7915a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7915a-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7915a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7915a-105">DESCRIPTION</span></span>
<span data-ttu-id="7915a-106">Polecenie **cmdlet Remove-AzApiManagementApiFromGateway** dołącza interfejs API do bramy.</span><span class="sxs-lookup"><span data-stu-id="7915a-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="7915a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7915a-107">EXAMPLES</span></span>

### <span data-ttu-id="7915a-108">Przykład 1. Usuwanie interfejsu API z bramy</span><span class="sxs-lookup"><span data-stu-id="7915a-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="7915a-109">To polecenie usuwa określony interfejs API z bramy.</span><span class="sxs-lookup"><span data-stu-id="7915a-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="7915a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7915a-110">PARAMETERS</span></span>

### <span data-ttu-id="7915a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7915a-111">-ApiId</span></span>
<span data-ttu-id="7915a-112">Identyfikator istniejących interfejsów API do usunięcia z bramy.</span><span class="sxs-lookup"><span data-stu-id="7915a-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="7915a-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7915a-113">This parameter is required.</span></span>

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

### <span data-ttu-id="7915a-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="7915a-114">-Context</span></span>
<span data-ttu-id="7915a-115">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7915a-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7915a-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7915a-116">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7915a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7915a-117">-DefaultProfile</span></span>
<span data-ttu-id="7915a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7915a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7915a-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="7915a-119">-GatewayId</span></span>
<span data-ttu-id="7915a-120">Identyfikator istniejącej bramy do usunięcia interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7915a-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="7915a-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7915a-121">This parameter is required.</span></span>

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

### <span data-ttu-id="7915a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7915a-122">-PassThru</span></span>
<span data-ttu-id="7915a-123">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="7915a-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="7915a-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7915a-124">This parameter is optional.</span></span>
<span data-ttu-id="7915a-125">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="7915a-125">Default value is false.</span></span>

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

### <span data-ttu-id="7915a-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7915a-126">-Confirm</span></span>
<span data-ttu-id="7915a-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7915a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7915a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7915a-128">-WhatIf</span></span>
<span data-ttu-id="7915a-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7915a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7915a-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7915a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7915a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7915a-131">CommonParameters</span></span>
<span data-ttu-id="7915a-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7915a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7915a-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7915a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7915a-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7915a-134">INPUTS</span></span>

### <span data-ttu-id="7915a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7915a-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7915a-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7915a-136">System.String</span></span>

### <span data-ttu-id="7915a-137">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="7915a-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7915a-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7915a-138">OUTPUTS</span></span>

### <span data-ttu-id="7915a-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7915a-139">System.Boolean</span></span>

## <span data-ttu-id="7915a-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7915a-140">NOTES</span></span>

## <span data-ttu-id="7915a-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7915a-141">RELATED LINKS</span></span>
