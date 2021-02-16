---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 9673df14bdd0f5b7d0e946170a155231e8c4e751
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412660"
---
# <span data-ttu-id="46b9c-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="46b9c-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="46b9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="46b9c-103">Usuwa określoną wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="46b9c-103">Removes a particular API Release</span></span>

## <span data-ttu-id="46b9c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46b9c-104">SYNTAX</span></span>

### <span data-ttu-id="46b9c-105">ByApiReleaseId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="46b9c-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="46b9c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="46b9c-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46b9c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="46b9c-107">DESCRIPTION</span></span>

<span data-ttu-id="46b9c-108">Polecenie **cmdlet Remove-AzAzureRmApiManagementApiRelease** usuwa istniejącą wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="46b9c-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="46b9c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46b9c-109">EXAMPLES</span></span>

### <span data-ttu-id="46b9c-110">Przykład 1. Usuwanie wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="46b9c-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="46b9c-111">To polecenie usuwa wersję interfejsu API z określonymi wartościami ApiId i ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="46b9c-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="46b9c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46b9c-112">PARAMETERS</span></span>

### <span data-ttu-id="46b9c-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="46b9c-113">-ApiId</span></span>
<span data-ttu-id="46b9c-114">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="46b9c-114">Identifier of the API.</span></span>
<span data-ttu-id="46b9c-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="46b9c-115">This parameter is required.</span></span>

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

### <span data-ttu-id="46b9c-116">— kontekst</span><span class="sxs-lookup"><span data-stu-id="46b9c-116">-Context</span></span>
<span data-ttu-id="46b9c-117">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="46b9c-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="46b9c-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="46b9c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="46b9c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b9c-119">-DefaultProfile</span></span>
<span data-ttu-id="46b9c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="46b9c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46b9c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="46b9c-121">-InputObject</span></span>
<span data-ttu-id="46b9c-122">Wystąpienie obiektu PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="46b9c-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="46b9c-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="46b9c-123">This parameter is required.</span></span>

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

### <span data-ttu-id="46b9c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="46b9c-124">-PassThru</span></span>
<span data-ttu-id="46b9c-125">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="46b9c-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="46b9c-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="46b9c-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="46b9c-127">- ReleaseId</span><span class="sxs-lookup"><span data-stu-id="46b9c-127">-ReleaseId</span></span>
<span data-ttu-id="46b9c-128">Identyfikator wydania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="46b9c-128">Identifier of the API Release.</span></span>
<span data-ttu-id="46b9c-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="46b9c-129">This parameter is required.</span></span>

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

### <span data-ttu-id="46b9c-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="46b9c-130">-Confirm</span></span>
<span data-ttu-id="46b9c-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="46b9c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46b9c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46b9c-132">-WhatIf</span></span>
<span data-ttu-id="46b9c-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46b9c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46b9c-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="46b9c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46b9c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b9c-135">CommonParameters</span></span>
<span data-ttu-id="46b9c-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b9c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b9c-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46b9c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b9c-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46b9c-138">INPUTS</span></span>

### <span data-ttu-id="46b9c-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="46b9c-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="46b9c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="46b9c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="46b9c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="46b9c-141">System.String</span></span>

## <span data-ttu-id="46b9c-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46b9c-142">OUTPUTS</span></span>

### <span data-ttu-id="46b9c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="46b9c-143">System.Boolean</span></span>

## <span data-ttu-id="46b9c-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46b9c-144">NOTES</span></span>

## <span data-ttu-id="46b9c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46b9c-145">RELATED LINKS</span></span>

[<span data-ttu-id="46b9c-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="46b9c-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="46b9c-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="46b9c-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="46b9c-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="46b9c-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)