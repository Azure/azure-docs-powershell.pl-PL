---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: cb7fbfe4ba4fdf09b9012ddc5be8028af0bd80c1
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93554416"
---
# <span data-ttu-id="ad4fa-101">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad4fa-101">New-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="ad4fa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4fa-103">Tworzenie wersji interfejsu API poprawki interfejsu API</span><span class="sxs-lookup"><span data-stu-id="ad4fa-103">Creates an API Release of an API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad4fa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad4fa-104">SYNTAX</span></span>

```
New-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ad4fa-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad4fa-105">DESCRIPTION</span></span>

<span data-ttu-id="ad4fa-106">Polecenie cmdlet **New-AzureRmApiManagementApiRelease** tworzy wersję API dla poprawki interfejsu API w kontekście zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-106">The **New-AzureRmApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="ad4fa-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad4fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ad4fa-108">Przykład 1: Tworzenie wersji interfejsu API dla wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="ad4fa-108">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


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

<span data-ttu-id="ad4fa-109">To polecenie tworzy wersję API poprawki `2` `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="ad4fa-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="ad4fa-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad4fa-110">PARAMETERS</span></span>

### <span data-ttu-id="ad4fa-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ad4fa-111">-ApiId</span></span>
<span data-ttu-id="ad4fa-112">Identyfikator nowego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="ad4fa-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="ad4fa-113">-ApiRevision</span></span>
<span data-ttu-id="ad4fa-114">Identyfikator poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="ad4fa-115">-Context</span><span class="sxs-lookup"><span data-stu-id="ad4fa-115">-Context</span></span>
<span data-ttu-id="ad4fa-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ad4fa-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-117">This parameter is required.</span></span>

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

### <span data-ttu-id="ad4fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4fa-118">-DefaultProfile</span></span>
<span data-ttu-id="ad4fa-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-120">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="ad4fa-120">-Note</span></span>
<span data-ttu-id="ad4fa-121">Informacje o wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-121">Api Release Notes.</span></span> <span data-ttu-id="ad4fa-122">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="ad4fa-122">This parameter is optional</span></span>

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

### <span data-ttu-id="ad4fa-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="ad4fa-123">-ReleaseId</span></span>
<span data-ttu-id="ad4fa-124">Identyfikator wersji API.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="ad4fa-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-125">This parameter is optional.</span></span>
<span data-ttu-id="ad4fa-126">Jeśli nie zostanie wygenerowany identyfikator.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="ad4fa-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad4fa-127">-Confirm</span></span>
<span data-ttu-id="ad4fa-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad4fa-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4fa-129">-WhatIf</span></span>
<span data-ttu-id="ad4fa-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad4fa-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad4fa-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4fa-132">CommonParameters</span></span>
<span data-ttu-id="ad4fa-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4fa-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4fa-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4fa-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad4fa-135">INPUTS</span></span>

### <span data-ttu-id="ad4fa-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad4fa-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="ad4fa-137">Parametry: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad4fa-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="ad4fa-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ad4fa-138">System.String</span></span>

## <span data-ttu-id="ad4fa-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad4fa-139">OUTPUTS</span></span>

### <span data-ttu-id="ad4fa-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad4fa-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="ad4fa-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad4fa-141">NOTES</span></span>

## <span data-ttu-id="ad4fa-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad4fa-142">RELATED LINKS</span></span>

[<span data-ttu-id="ad4fa-143">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad4fa-143">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="ad4fa-144">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad4fa-144">Remove-AzureRmApiManagementApiRelease</span></span>](./Remove-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="ad4fa-145">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad4fa-145">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
