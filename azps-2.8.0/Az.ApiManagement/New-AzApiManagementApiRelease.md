---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 5a5d155b8c9127d330a1f53d1fe53d42d60d46a8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406608"
---
# <span data-ttu-id="4cf64-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4cf64-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="4cf64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf64-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf64-103">Tworzy wersję interfejsu API poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="4cf64-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="4cf64-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4cf64-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4cf64-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4cf64-105">DESCRIPTION</span></span>

<span data-ttu-id="4cf64-106">Polecenie **cmdlet New-AzApiManagementApiRelease** tworzy wersję interfejsu API dla poprawki interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="4cf64-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="4cf64-107">Wersja służy do zmiany poprawki interfejsu API jako bieżącej poprawki.</span><span class="sxs-lookup"><span data-stu-id="4cf64-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="4cf64-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4cf64-108">EXAMPLES</span></span>

### <span data-ttu-id="4cf64-109">Przykład 1. Tworzenie wersji interfejsu API dla poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="4cf64-109">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="4cf64-110">To polecenie tworzy wersję poprawki interfejsu `2` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="4cf64-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="4cf64-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cf64-111">PARAMETERS</span></span>

### <span data-ttu-id="4cf64-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4cf64-112">-ApiId</span></span>
<span data-ttu-id="4cf64-113">Identyfikator nowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4cf64-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="4cf64-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="4cf64-114">-ApiRevision</span></span>
<span data-ttu-id="4cf64-115">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4cf64-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="4cf64-116">— kontekst</span><span class="sxs-lookup"><span data-stu-id="4cf64-116">-Context</span></span>
<span data-ttu-id="4cf64-117">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4cf64-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4cf64-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="4cf64-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cf64-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf64-119">-DefaultProfile</span></span>
<span data-ttu-id="4cf64-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4cf64-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf64-121">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="4cf64-121">-Note</span></span>
<span data-ttu-id="4cf64-122">Informacje o wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4cf64-122">Api Release Notes.</span></span> <span data-ttu-id="4cf64-123">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="4cf64-123">This parameter is optional</span></span>

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

### <span data-ttu-id="4cf64-124">- ReleaseId</span><span class="sxs-lookup"><span data-stu-id="4cf64-124">-ReleaseId</span></span>
<span data-ttu-id="4cf64-125">Identyfikator wydania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4cf64-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="4cf64-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="4cf64-126">This parameter is optional.</span></span>
<span data-ttu-id="4cf64-127">Jeśli nie zostanie określony identyfikator, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="4cf64-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="4cf64-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4cf64-128">-Confirm</span></span>
<span data-ttu-id="4cf64-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4cf64-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cf64-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf64-130">-WhatIf</span></span>
<span data-ttu-id="4cf64-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4cf64-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4cf64-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4cf64-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cf64-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf64-133">CommonParameters</span></span>
<span data-ttu-id="4cf64-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cf64-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf64-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cf64-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf64-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cf64-136">INPUTS</span></span>

### <span data-ttu-id="4cf64-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4cf64-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4cf64-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4cf64-138">System.String</span></span>

## <span data-ttu-id="4cf64-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4cf64-139">OUTPUTS</span></span>

### <span data-ttu-id="4cf64-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4cf64-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="4cf64-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4cf64-141">NOTES</span></span>

## <span data-ttu-id="4cf64-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4cf64-142">RELATED LINKS</span></span>

[<span data-ttu-id="4cf64-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4cf64-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="4cf64-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4cf64-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="4cf64-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="4cf64-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)