---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 51a24bcb0951aef7a3feb8b32d3d860d21839ad5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407934"
---
# <span data-ttu-id="62ae4-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="62ae4-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="62ae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62ae4-102">SYNOPSIS</span></span>
<span data-ttu-id="62ae4-103">Usuwa określoną wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="62ae4-103">Removes a particular API Release</span></span>

## <span data-ttu-id="62ae4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62ae4-104">SYNTAX</span></span>

### <span data-ttu-id="62ae4-105">ByApiReleaseId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="62ae4-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62ae4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="62ae4-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62ae4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="62ae4-107">DESCRIPTION</span></span>

<span data-ttu-id="62ae4-108">Polecenie **cmdlet Remove-AzAzureRmApiManagementApiRelease** usuwa istniejącą wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="62ae4-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="62ae4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62ae4-109">EXAMPLES</span></span>

### <span data-ttu-id="62ae4-110">Przykład 1. Usuwanie wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="62ae4-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="62ae4-111">To polecenie usuwa wersję interfejsu API z określonymi wartościami ApiId i ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="62ae4-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="62ae4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62ae4-112">PARAMETERS</span></span>

### <span data-ttu-id="62ae4-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="62ae4-113">-ApiId</span></span>
<span data-ttu-id="62ae4-114">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="62ae4-114">Identifier of the API.</span></span>
<span data-ttu-id="62ae4-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="62ae4-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62ae4-116">— kontekst</span><span class="sxs-lookup"><span data-stu-id="62ae4-116">-Context</span></span>
<span data-ttu-id="62ae4-117">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="62ae4-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="62ae4-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="62ae4-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62ae4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62ae4-119">-DefaultProfile</span></span>
<span data-ttu-id="62ae4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62ae4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62ae4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62ae4-121">-InputObject</span></span>
<span data-ttu-id="62ae4-122">Wystąpienie obiektu PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="62ae4-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="62ae4-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="62ae4-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62ae4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="62ae4-124">-PassThru</span></span>
<span data-ttu-id="62ae4-125">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="62ae4-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="62ae4-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="62ae4-126">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62ae4-127">- ReleaseId</span><span class="sxs-lookup"><span data-stu-id="62ae4-127">-ReleaseId</span></span>
<span data-ttu-id="62ae4-128">Identyfikator wydania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="62ae4-128">Identifier of the API Release.</span></span>
<span data-ttu-id="62ae4-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="62ae4-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiReleaseId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62ae4-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62ae4-130">-Confirm</span></span>
<span data-ttu-id="62ae4-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="62ae4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ae4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ae4-132">-WhatIf</span></span>
<span data-ttu-id="62ae4-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ae4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62ae4-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="62ae4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ae4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62ae4-135">CommonParameters</span></span>
<span data-ttu-id="62ae4-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62ae4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62ae4-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62ae4-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62ae4-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62ae4-138">INPUTS</span></span>

### <span data-ttu-id="62ae4-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="62ae4-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="62ae4-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="62ae4-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="62ae4-141">System.String</span><span class="sxs-lookup"><span data-stu-id="62ae4-141">System.String</span></span>

## <span data-ttu-id="62ae4-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62ae4-142">OUTPUTS</span></span>

### <span data-ttu-id="62ae4-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="62ae4-143">System.Boolean</span></span>

## <span data-ttu-id="62ae4-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62ae4-144">NOTES</span></span>

## <span data-ttu-id="62ae4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62ae4-145">RELATED LINKS</span></span>

[<span data-ttu-id="62ae4-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="62ae4-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="62ae4-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="62ae4-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="62ae4-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="62ae4-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)