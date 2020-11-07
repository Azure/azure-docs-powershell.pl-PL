---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: f6f042f26f5dede90db77e8c373e337f00755001
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869307"
---
# <span data-ttu-id="7761c-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7761c-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="7761c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7761c-102">SYNOPSIS</span></span>
<span data-ttu-id="7761c-103">Aktualizuje określoną wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7761c-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="7761c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7761c-104">SYNTAX</span></span>

### <span data-ttu-id="7761c-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7761c-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7761c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7761c-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7761c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7761c-107">DESCRIPTION</span></span>
<span data-ttu-id="7761c-108">Polecenie cmdlet **Update-AzApiManagementApiRelease** modyfikuje wersję interfejsu API zarządzania usługą Azure API.</span><span class="sxs-lookup"><span data-stu-id="7761c-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="7761c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7761c-109">EXAMPLES</span></span>

### <span data-ttu-id="7761c-110">Przykład 1: Aktualizacja wersji interfejsu API dla wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="7761c-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="7761c-111">To polecenie aktualizuje `echo-api-release` wersję API interfejsu API `echo-api` przy użyciu nowej notatki.</span><span class="sxs-lookup"><span data-stu-id="7761c-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="7761c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7761c-112">PARAMETERS</span></span>

### <span data-ttu-id="7761c-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7761c-113">-ApiId</span></span>
<span data-ttu-id="7761c-114">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7761c-114">Identifier of existing API.</span></span>
<span data-ttu-id="7761c-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7761c-115">This parameter is required.</span></span>

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

### <span data-ttu-id="7761c-116">-Context</span><span class="sxs-lookup"><span data-stu-id="7761c-116">-Context</span></span>
<span data-ttu-id="7761c-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7761c-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7761c-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7761c-118">This parameter is required.</span></span>

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

### <span data-ttu-id="7761c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7761c-119">-DefaultProfile</span></span>
<span data-ttu-id="7761c-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7761c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7761c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7761c-121">-InputObject</span></span>
<span data-ttu-id="7761c-122">Wystąpienie typu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="7761c-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="7761c-123">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="7761c-123">-Note</span></span>
<span data-ttu-id="7761c-124">Informacje o wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7761c-124">Api Release Notes.</span></span>
<span data-ttu-id="7761c-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7761c-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="7761c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7761c-126">-PassThru</span></span>
<span data-ttu-id="7761c-127">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApiRelease reprezentujące zestaw interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="7761c-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="7761c-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="7761c-128">-ReleaseId</span></span>
<span data-ttu-id="7761c-129">Identyfikator ReleaseId poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7761c-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="7761c-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7761c-130">This parameter is required.</span></span>

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

### <span data-ttu-id="7761c-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7761c-131">-Confirm</span></span>
<span data-ttu-id="7761c-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7761c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7761c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7761c-133">-WhatIf</span></span>
<span data-ttu-id="7761c-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7761c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7761c-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7761c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7761c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7761c-136">CommonParameters</span></span>
<span data-ttu-id="7761c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7761c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7761c-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7761c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7761c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7761c-139">INPUTS</span></span>

### <span data-ttu-id="7761c-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7761c-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7761c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="7761c-141">System.String</span></span>

### <span data-ttu-id="7761c-142">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7761c-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="7761c-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7761c-143">OUTPUTS</span></span>

### <span data-ttu-id="7761c-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7761c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="7761c-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7761c-145">NOTES</span></span>

## <span data-ttu-id="7761c-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7761c-146">RELATED LINKS</span></span>

[<span data-ttu-id="7761c-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7761c-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="7761c-148">Nowe — AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="7761c-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
