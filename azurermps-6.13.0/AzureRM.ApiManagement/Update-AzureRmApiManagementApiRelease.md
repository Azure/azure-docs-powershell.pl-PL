---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 5b863c0d0c808c8cb993e4f78f9767d13fb634d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526362"
---
# <span data-ttu-id="ad891-101">Update-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad891-101">Update-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="ad891-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad891-102">SYNOPSIS</span></span>
<span data-ttu-id="ad891-103">Aktualizuje określoną wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ad891-103">Updates a particular Api Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad891-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad891-104">SYNTAX</span></span>

### <span data-ttu-id="ad891-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ad891-105">ExpandedParameter (Default)</span></span>
```
Update-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad891-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ad891-106">ByInputObject</span></span>
```
Update-AzureRmApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad891-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ad891-107">DESCRIPTION</span></span>
<span data-ttu-id="ad891-108">Polecenie cmdlet **Update-AzureRmApiManagementApiRelease** modyfikuje wersję interfejsu API zarządzania usługą Azure API.</span><span class="sxs-lookup"><span data-stu-id="ad891-108">The **Update-AzureRmApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="ad891-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad891-109">EXAMPLES</span></span>

### <span data-ttu-id="ad891-110">Przykład 1: Aktualizacja wersji interfejsu API dla wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="ad891-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="ad891-111">To polecenie aktualizuje `echo-api-release` wersję API interfejsu API `echo-api` przy użyciu nowej notatki.</span><span class="sxs-lookup"><span data-stu-id="ad891-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="ad891-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad891-112">PARAMETERS</span></span>

### <span data-ttu-id="ad891-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ad891-113">-ApiId</span></span>
<span data-ttu-id="ad891-114">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ad891-114">Identifier of existing API.</span></span>
<span data-ttu-id="ad891-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ad891-115">This parameter is required.</span></span>

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

### <span data-ttu-id="ad891-116">-Context</span><span class="sxs-lookup"><span data-stu-id="ad891-116">-Context</span></span>
<span data-ttu-id="ad891-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ad891-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ad891-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ad891-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ad891-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad891-119">-DefaultProfile</span></span>
<span data-ttu-id="ad891-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad891-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad891-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ad891-121">-InputObject</span></span>
<span data-ttu-id="ad891-122">Wystąpienie typu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="ad891-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="ad891-123">-Uwaga</span><span class="sxs-lookup"><span data-stu-id="ad891-123">-Note</span></span>
<span data-ttu-id="ad891-124">Informacje o wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ad891-124">Api Release Notes.</span></span>
<span data-ttu-id="ad891-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ad891-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="ad891-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ad891-126">-PassThru</span></span>
<span data-ttu-id="ad891-127">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApiRelease reprezentujące zestaw interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="ad891-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="ad891-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="ad891-128">-ReleaseId</span></span>
<span data-ttu-id="ad891-129">Identyfikator ReleaseId poprawki interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ad891-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="ad891-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ad891-130">This parameter is required.</span></span>

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

### <span data-ttu-id="ad891-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad891-131">-Confirm</span></span>
<span data-ttu-id="ad891-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad891-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad891-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad891-133">-WhatIf</span></span>
<span data-ttu-id="ad891-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad891-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad891-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad891-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad891-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad891-136">CommonParameters</span></span>
<span data-ttu-id="ad891-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad891-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad891-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad891-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad891-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad891-139">INPUTS</span></span>

### <span data-ttu-id="ad891-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ad891-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="ad891-141">Parametry: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ad891-141">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="ad891-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ad891-142">System.String</span></span>

### <span data-ttu-id="ad891-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad891-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="ad891-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad891-144">OUTPUTS</span></span>

### <span data-ttu-id="ad891-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad891-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="ad891-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad891-146">NOTES</span></span>

## <span data-ttu-id="ad891-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad891-147">RELATED LINKS</span></span>

[<span data-ttu-id="ad891-148">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad891-148">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="ad891-149">Nowe — AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="ad891-149">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)
