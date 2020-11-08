---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 9b2b94fbd6a308f9d927483e78e060a273354738
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053964"
---
# <span data-ttu-id="a466a-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a466a-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="a466a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a466a-102">SYNOPSIS</span></span>
<span data-ttu-id="a466a-103">Tworzenie wersji interfejsu API poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="a466a-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="a466a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a466a-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a466a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a466a-105">DESCRIPTION</span></span>

<span data-ttu-id="a466a-106">Polecenie cmdlet **New-AzApiManagementApiRelease** tworzy wersję API dla poprawki interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="a466a-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="a466a-107">Wersja jest używana w celu dokonania korekty interfejsu API jako bieżącej wersji.</span><span class="sxs-lookup"><span data-stu-id="a466a-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="a466a-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a466a-108">EXAMPLES</span></span>

### <span data-ttu-id="a466a-109">Przykład 1: Tworzenie wersji interfejsu API dla wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="a466a-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="a466a-110">To polecenie tworzy wersję API poprawki `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="a466a-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="a466a-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a466a-111">PARAMETERS</span></span>

### <span data-ttu-id="a466a-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a466a-112">-ApiId</span></span>
<span data-ttu-id="a466a-113">Identyfikator nowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a466a-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="a466a-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="a466a-114">-ApiRevision</span></span>
<span data-ttu-id="a466a-115">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a466a-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="a466a-116">-Context</span><span class="sxs-lookup"><span data-stu-id="a466a-116">-Context</span></span>
<span data-ttu-id="a466a-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a466a-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a466a-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a466a-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a466a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a466a-119">-DefaultProfile</span></span>
<span data-ttu-id="a466a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a466a-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a466a-121">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="a466a-121">-Note</span></span>
<span data-ttu-id="a466a-122">Informacje o wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a466a-122">Api Release Notes.</span></span> <span data-ttu-id="a466a-123">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="a466a-123">This parameter is optional</span></span>

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

### <span data-ttu-id="a466a-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="a466a-124">-ReleaseId</span></span>
<span data-ttu-id="a466a-125">Identyfikator wersji API.</span><span class="sxs-lookup"><span data-stu-id="a466a-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="a466a-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a466a-126">This parameter is optional.</span></span>
<span data-ttu-id="a466a-127">Jeśli nie zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="a466a-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="a466a-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a466a-128">-Confirm</span></span>
<span data-ttu-id="a466a-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a466a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a466a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a466a-130">-WhatIf</span></span>
<span data-ttu-id="a466a-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a466a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a466a-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a466a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a466a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a466a-133">CommonParameters</span></span>
<span data-ttu-id="a466a-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a466a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a466a-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a466a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a466a-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a466a-136">INPUTS</span></span>

### <span data-ttu-id="a466a-137">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a466a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a466a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="a466a-138">System.String</span></span>

## <span data-ttu-id="a466a-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a466a-139">OUTPUTS</span></span>

### <span data-ttu-id="a466a-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a466a-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a466a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a466a-141">NOTES</span></span>

## <span data-ttu-id="a466a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a466a-142">RELATED LINKS</span></span>

[<span data-ttu-id="a466a-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a466a-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="a466a-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a466a-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="a466a-145">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a466a-145">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)