---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromGateway.md
ms.openlocfilehash: 506287812f684a778fdb96e750aac34049912b58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358379"
---
# <span data-ttu-id="08f29-101">Remove-AzApiManagementApiFromGateway</span><span class="sxs-lookup"><span data-stu-id="08f29-101">Remove-AzApiManagementApiFromGateway</span></span>

## <span data-ttu-id="08f29-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08f29-102">SYNOPSIS</span></span>
<span data-ttu-id="08f29-103">Dołącza interfejs API do bramy.</span><span class="sxs-lookup"><span data-stu-id="08f29-103">Attaches an API to a gateway.</span></span>

## <span data-ttu-id="08f29-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08f29-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromGateway -Context <PsApiManagementContext> -GatewayId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08f29-105">Opis</span><span class="sxs-lookup"><span data-stu-id="08f29-105">DESCRIPTION</span></span>
<span data-ttu-id="08f29-106">Polecenie cmdlet **Remove-AzApiManagementApiFromGateway** dołącza interfejs API do bramy.</span><span class="sxs-lookup"><span data-stu-id="08f29-106">The **Remove-AzApiManagementApiFromGateway** cmdlet attaches an API to a gateway.</span></span>

## <span data-ttu-id="08f29-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08f29-107">EXAMPLES</span></span>

### <span data-ttu-id="08f29-108">Przykład 1: Usuwanie interfejsu API z bramy</span><span class="sxs-lookup"><span data-stu-id="08f29-108">Example 1: Remove an API from a gateway</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromGateway -Context $ApiMgmtContext -GatewayId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="08f29-109">To polecenie usuwa określony interfejs API z bramy.</span><span class="sxs-lookup"><span data-stu-id="08f29-109">This command removes the specified API from a gateway.</span></span>

## <span data-ttu-id="08f29-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08f29-110">PARAMETERS</span></span>

### <span data-ttu-id="08f29-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="08f29-111">-ApiId</span></span>
<span data-ttu-id="08f29-112">Identyfikator istniejących interfejsów API do usunięcia z bramy.</span><span class="sxs-lookup"><span data-stu-id="08f29-112">Identifier of existing APIs to remove from the Gateway.</span></span>
<span data-ttu-id="08f29-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="08f29-113">This parameter is required.</span></span>

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

### <span data-ttu-id="08f29-114">-Context</span><span class="sxs-lookup"><span data-stu-id="08f29-114">-Context</span></span>
<span data-ttu-id="08f29-115">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="08f29-115">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="08f29-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="08f29-116">This parameter is required.</span></span>

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

### <span data-ttu-id="08f29-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f29-117">-DefaultProfile</span></span>
<span data-ttu-id="08f29-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08f29-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f29-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="08f29-119">-GatewayId</span></span>
<span data-ttu-id="08f29-120">Identyfikator istniejącej bramy, z której ma zostać usunięty interfejs API.</span><span class="sxs-lookup"><span data-stu-id="08f29-120">Identifier of existing Gateway to remove API from.</span></span>
<span data-ttu-id="08f29-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="08f29-121">This parameter is required.</span></span>

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

### <span data-ttu-id="08f29-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08f29-122">-PassThru</span></span>
<span data-ttu-id="08f29-123">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="08f29-123">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="08f29-124">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="08f29-124">This parameter is optional.</span></span>
<span data-ttu-id="08f29-125">Wartość domyślna to false.</span><span class="sxs-lookup"><span data-stu-id="08f29-125">Default value is false.</span></span>

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

### <span data-ttu-id="08f29-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08f29-126">-Confirm</span></span>
<span data-ttu-id="08f29-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08f29-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f29-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f29-128">-WhatIf</span></span>
<span data-ttu-id="08f29-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08f29-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="08f29-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08f29-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f29-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f29-131">CommonParameters</span></span>
<span data-ttu-id="08f29-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f29-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f29-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08f29-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f29-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08f29-134">INPUTS</span></span>

### <span data-ttu-id="08f29-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="08f29-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="08f29-136">System. String</span><span class="sxs-lookup"><span data-stu-id="08f29-136">System.String</span></span>

### <span data-ttu-id="08f29-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="08f29-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="08f29-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08f29-138">OUTPUTS</span></span>

### <span data-ttu-id="08f29-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08f29-139">System.Boolean</span></span>

## <span data-ttu-id="08f29-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08f29-140">NOTES</span></span>

## <span data-ttu-id="08f29-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08f29-141">RELATED LINKS</span></span>
