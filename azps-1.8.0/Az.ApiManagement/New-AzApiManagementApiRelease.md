---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 5e536d3174a9a71cf4f648172f3d06e6fc5ae79f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401007"
---
# <span data-ttu-id="f0f9d-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f0f9d-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="f0f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="f0f9d-103">Tworzy wersję interfejsu API poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="f0f9d-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="f0f9d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f0f9d-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f0f9d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f0f9d-105">DESCRIPTION</span></span>

<span data-ttu-id="f0f9d-106">Polecenie **cmdlet New-AzApiManagementApiRelease** tworzy wersję interfejsu API dla poprawki interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="f0f9d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f0f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="f0f9d-108">Przykład 1. Tworzenie wersji interfejsu API dla poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="f0f9d-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="f0f9d-109">To polecenie tworzy wersję wersji poprawki interfejsu `2` `echo-api` API.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="f0f9d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0f9d-110">PARAMETERS</span></span>

### <span data-ttu-id="f0f9d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f0f9d-111">-ApiId</span></span>
<span data-ttu-id="f0f9d-112">Identyfikator nowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="f0f9d-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f0f9d-113">-ApiRevision</span></span>
<span data-ttu-id="f0f9d-114">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="f0f9d-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="f0f9d-115">-Context</span></span>
<span data-ttu-id="f0f9d-116">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f0f9d-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-117">This parameter is required.</span></span>

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

### <span data-ttu-id="f0f9d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0f9d-118">-DefaultProfile</span></span>
<span data-ttu-id="f0f9d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0f9d-120">— Uwaga</span><span class="sxs-lookup"><span data-stu-id="f0f9d-120">-Note</span></span>
<span data-ttu-id="f0f9d-121">Informacje o wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-121">Api Release Notes.</span></span> <span data-ttu-id="f0f9d-122">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="f0f9d-122">This parameter is optional</span></span>

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

### <span data-ttu-id="f0f9d-123">- ReleaseId</span><span class="sxs-lookup"><span data-stu-id="f0f9d-123">-ReleaseId</span></span>
<span data-ttu-id="f0f9d-124">Identyfikator wydania interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="f0f9d-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-125">This parameter is optional.</span></span>
<span data-ttu-id="f0f9d-126">Jeśli nie zostanie określony identyfikator, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="f0f9d-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0f9d-127">-Confirm</span></span>
<span data-ttu-id="f0f9d-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0f9d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0f9d-129">-WhatIf</span></span>
<span data-ttu-id="f0f9d-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0f9d-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0f9d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0f9d-132">CommonParameters</span></span>
<span data-ttu-id="f0f9d-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0f9d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0f9d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0f9d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0f9d-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0f9d-135">INPUTS</span></span>

### <span data-ttu-id="f0f9d-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f0f9d-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f0f9d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f0f9d-137">System.String</span></span>

## <span data-ttu-id="f0f9d-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0f9d-138">OUTPUTS</span></span>

### <span data-ttu-id="f0f9d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f0f9d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="f0f9d-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f0f9d-140">NOTES</span></span>

## <span data-ttu-id="f0f9d-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0f9d-141">RELATED LINKS</span></span>

[<span data-ttu-id="f0f9d-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f0f9d-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="f0f9d-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f0f9d-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="f0f9d-144">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="f0f9d-144">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)