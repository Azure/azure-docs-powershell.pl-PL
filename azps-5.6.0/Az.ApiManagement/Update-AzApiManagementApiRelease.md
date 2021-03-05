---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 16c73a389e6602999272255534312928fc4a13f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978938"
---
# <span data-ttu-id="9a5fd-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9a5fd-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="9a5fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a5fd-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5fd-103">Aktualizuje określoną wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="9a5fd-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a5fd-104">SYNTAX</span></span>

### <span data-ttu-id="9a5fd-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9a5fd-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a5fd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9a5fd-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a5fd-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a5fd-107">DESCRIPTION</span></span>
<span data-ttu-id="9a5fd-108">Polecenie **cmdlet Update-AzApiManagementApiRelease modyfikuje** wersję interfejsu API zarządzania interfejsem API platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="9a5fd-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a5fd-109">EXAMPLES</span></span>

### <span data-ttu-id="9a5fd-110">Przykład 1. Aktualizacja wersji interfejsu API dla poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="9a5fd-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="9a5fd-111">To polecenie aktualizuje wersję `echo-api-release` interfejsu API za `echo-api` pomocą nowej notatki.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="9a5fd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a5fd-112">PARAMETERS</span></span>

### <span data-ttu-id="9a5fd-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9a5fd-113">-ApiId</span></span>
<span data-ttu-id="9a5fd-114">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-114">Identifier of existing API.</span></span>
<span data-ttu-id="9a5fd-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-115">This parameter is required.</span></span>

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

### <span data-ttu-id="9a5fd-116">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9a5fd-116">-Context</span></span>
<span data-ttu-id="9a5fd-117">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9a5fd-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5fd-119">-DefaultProfile</span></span>
<span data-ttu-id="9a5fd-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a5fd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a5fd-121">-InputObject</span></span>
<span data-ttu-id="9a5fd-122">Wystąpienie typu Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5fd-123">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="9a5fd-123">-Note</span></span>
<span data-ttu-id="9a5fd-124">Informacje o wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-124">Api Release Notes.</span></span>
<span data-ttu-id="9a5fd-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="9a5fd-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a5fd-126">-PassThru</span></span>
<span data-ttu-id="9a5fd-127">Jeśli określono, wówczas wystąpienie microsoft.azure.commands.apiManagement.ServiceManagement.Models.PsApiManagementApiRelease typ reprezentujący ustawiną wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="9a5fd-128">- ReleaseId</span><span class="sxs-lookup"><span data-stu-id="9a5fd-128">-ReleaseId</span></span>
<span data-ttu-id="9a5fd-129">Identyfikator identyfikatora Api Revision ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="9a5fd-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-130">This parameter is required.</span></span>

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

### <span data-ttu-id="9a5fd-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a5fd-131">-Confirm</span></span>
<span data-ttu-id="9a5fd-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a5fd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a5fd-133">-WhatIf</span></span>
<span data-ttu-id="9a5fd-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a5fd-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a5fd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5fd-136">CommonParameters</span></span>
<span data-ttu-id="9a5fd-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5fd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5fd-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a5fd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5fd-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a5fd-139">INPUTS</span></span>

### <span data-ttu-id="9a5fd-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9a5fd-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9a5fd-141">System.String</span><span class="sxs-lookup"><span data-stu-id="9a5fd-141">System.String</span></span>

### <span data-ttu-id="9a5fd-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9a5fd-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="9a5fd-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a5fd-143">OUTPUTS</span></span>

### <span data-ttu-id="9a5fd-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9a5fd-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="9a5fd-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a5fd-145">NOTES</span></span>

## <span data-ttu-id="9a5fd-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a5fd-146">RELATED LINKS</span></span>

[<span data-ttu-id="9a5fd-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9a5fd-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="9a5fd-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9a5fd-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
