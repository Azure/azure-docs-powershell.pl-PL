---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: f816488e6334c0e9c410bb1c24f46501a1fefe85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704613"
---
# <span data-ttu-id="d51a5-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d51a5-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="d51a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d51a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d51a5-103">Tworzenie wersji interfejsu API poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="d51a5-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="d51a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d51a5-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d51a5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d51a5-105">DESCRIPTION</span></span>

<span data-ttu-id="d51a5-106">Polecenie cmdlet **New-AzApiManagementApiRelease** tworzy wersję API dla poprawki interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d51a5-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="d51a5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d51a5-107">EXAMPLES</span></span>

### <span data-ttu-id="d51a5-108">Przykład 1: Tworzenie wersji interfejsu API dla wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="d51a5-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="d51a5-109">To polecenie tworzy wersję API poprawki `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="d51a5-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="d51a5-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d51a5-110">PARAMETERS</span></span>

### <span data-ttu-id="d51a5-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d51a5-111">-ApiId</span></span>
<span data-ttu-id="d51a5-112">Identyfikator nowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d51a5-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="d51a5-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="d51a5-113">-ApiRevision</span></span>
<span data-ttu-id="d51a5-114">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d51a5-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="d51a5-115">-Context</span><span class="sxs-lookup"><span data-stu-id="d51a5-115">-Context</span></span>
<span data-ttu-id="d51a5-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d51a5-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d51a5-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d51a5-117">This parameter is required.</span></span>

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

### <span data-ttu-id="d51a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d51a5-118">-DefaultProfile</span></span>
<span data-ttu-id="d51a5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d51a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d51a5-120">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="d51a5-120">-Note</span></span>
<span data-ttu-id="d51a5-121">Informacje o wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d51a5-121">Api Release Notes.</span></span> <span data-ttu-id="d51a5-122">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="d51a5-122">This parameter is optional</span></span>

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

### <span data-ttu-id="d51a5-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="d51a5-123">-ReleaseId</span></span>
<span data-ttu-id="d51a5-124">Identyfikator wersji API.</span><span class="sxs-lookup"><span data-stu-id="d51a5-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="d51a5-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d51a5-125">This parameter is optional.</span></span>
<span data-ttu-id="d51a5-126">Jeśli nie zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="d51a5-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="d51a5-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d51a5-127">-Confirm</span></span>
<span data-ttu-id="d51a5-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d51a5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d51a5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d51a5-129">-WhatIf</span></span>
<span data-ttu-id="d51a5-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d51a5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d51a5-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d51a5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d51a5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d51a5-132">CommonParameters</span></span>
<span data-ttu-id="d51a5-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d51a5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d51a5-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d51a5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d51a5-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d51a5-135">INPUTS</span></span>

### <span data-ttu-id="d51a5-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d51a5-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d51a5-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d51a5-137">System.String</span></span>

## <span data-ttu-id="d51a5-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d51a5-138">OUTPUTS</span></span>

### <span data-ttu-id="d51a5-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d51a5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="d51a5-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d51a5-140">NOTES</span></span>

## <span data-ttu-id="d51a5-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d51a5-141">RELATED LINKS</span></span>

[<span data-ttu-id="d51a5-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d51a5-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="d51a5-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d51a5-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="d51a5-144">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="d51a5-144">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)