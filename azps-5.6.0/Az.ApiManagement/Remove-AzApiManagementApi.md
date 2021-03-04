---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApi.md
ms.openlocfilehash: d1ef516fc8b95814685350eb309e0a56d08d4b59
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959114"
---
# <span data-ttu-id="5245a-101">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5245a-101">Remove-AzApiManagementApi</span></span>

## <span data-ttu-id="5245a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5245a-102">SYNOPSIS</span></span>
<span data-ttu-id="5245a-103">Usuwa interfejs API.</span><span class="sxs-lookup"><span data-stu-id="5245a-103">Removes an API.</span></span>

## <span data-ttu-id="5245a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5245a-104">SYNTAX</span></span>

```
Remove-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5245a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5245a-105">DESCRIPTION</span></span>
<span data-ttu-id="5245a-106">Polecenie **cmdlet Remove-AzApiManagementApi** usuwa istniejący interfejs API.</span><span class="sxs-lookup"><span data-stu-id="5245a-106">The **Remove-AzApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="5245a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5245a-107">EXAMPLES</span></span>

### <span data-ttu-id="5245a-108">Przykład 1. Usuwanie interfejsu API</span><span class="sxs-lookup"><span data-stu-id="5245a-108">Example 1: Remove an API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApi -Context $apimContext -ApiId "0123456789"
```

<span data-ttu-id="5245a-109">To polecenie usuwa interfejs API z określonym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="5245a-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="5245a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5245a-110">PARAMETERS</span></span>

### <span data-ttu-id="5245a-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5245a-111">-ApiId</span></span>
<span data-ttu-id="5245a-112">Określa identyfikator usuwania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5245a-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="5245a-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="5245a-113">-Context</span></span>
<span data-ttu-id="5245a-114">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="5245a-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="5245a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5245a-115">-DefaultProfile</span></span>
<span data-ttu-id="5245a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5245a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5245a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5245a-117">-PassThru</span></span>
<span data-ttu-id="5245a-118">passthru</span><span class="sxs-lookup"><span data-stu-id="5245a-118">passthru</span></span>

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

### <span data-ttu-id="5245a-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5245a-119">-Confirm</span></span>
<span data-ttu-id="5245a-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5245a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5245a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5245a-121">-WhatIf</span></span>
<span data-ttu-id="5245a-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5245a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5245a-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5245a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5245a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5245a-124">CommonParameters</span></span>
<span data-ttu-id="5245a-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5245a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5245a-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5245a-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5245a-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5245a-127">INPUTS</span></span>

### <span data-ttu-id="5245a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5245a-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5245a-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5245a-129">System.String</span></span>

### <span data-ttu-id="5245a-130">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="5245a-130">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5245a-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5245a-131">OUTPUTS</span></span>

### <span data-ttu-id="5245a-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5245a-132">System.Boolean</span></span>

## <span data-ttu-id="5245a-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5245a-133">NOTES</span></span>

## <span data-ttu-id="5245a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5245a-134">RELATED LINKS</span></span>

[<span data-ttu-id="5245a-135">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5245a-135">Export-AzApiManagementApi</span></span>](./Export-AzApiManagementApi.md)

[<span data-ttu-id="5245a-136">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5245a-136">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="5245a-137">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5245a-137">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="5245a-138">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5245a-138">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="5245a-139">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="5245a-139">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


