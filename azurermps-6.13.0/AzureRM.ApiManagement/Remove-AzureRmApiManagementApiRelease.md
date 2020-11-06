---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524726"
---
# <span data-ttu-id="38b0d-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="38b0d-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="38b0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="38b0d-103">Usuwa określoną wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="38b0d-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38b0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38b0d-104">SYNTAX</span></span>

### <span data-ttu-id="38b0d-105">ByApiReleaseId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="38b0d-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38b0d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="38b0d-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38b0d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="38b0d-107">DESCRIPTION</span></span>

<span data-ttu-id="38b0d-108">Polecenie cmdlet **Remove-AzureRmApiManagementApiRelease** Usuwa istniejącą wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="38b0d-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="38b0d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38b0d-109">EXAMPLES</span></span>

### <span data-ttu-id="38b0d-110">Przykład 1: Usuwanie wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="38b0d-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="38b0d-111">To polecenie powoduje usunięcie wersji interfejsu API z określonym ApiId i ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="38b0d-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="38b0d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38b0d-112">PARAMETERS</span></span>

### <span data-ttu-id="38b0d-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="38b0d-113">-ApiId</span></span>
<span data-ttu-id="38b0d-114">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="38b0d-114">Identifier of the API.</span></span>
<span data-ttu-id="38b0d-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="38b0d-115">This parameter is required.</span></span>

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

### <span data-ttu-id="38b0d-116">-Context</span><span class="sxs-lookup"><span data-stu-id="38b0d-116">-Context</span></span>
<span data-ttu-id="38b0d-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="38b0d-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="38b0d-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="38b0d-118">This parameter is required.</span></span>

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

### <span data-ttu-id="38b0d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b0d-119">-DefaultProfile</span></span>
<span data-ttu-id="38b0d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="38b0d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38b0d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="38b0d-121">-InputObject</span></span>
<span data-ttu-id="38b0d-122">Wystąpienie PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="38b0d-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="38b0d-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="38b0d-123">This parameter is required.</span></span>

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

### <span data-ttu-id="38b0d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38b0d-124">-PassThru</span></span>
<span data-ttu-id="38b0d-125">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="38b0d-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="38b0d-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="38b0d-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="38b0d-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="38b0d-127">-ReleaseId</span></span>
<span data-ttu-id="38b0d-128">Identyfikator wersji API.</span><span class="sxs-lookup"><span data-stu-id="38b0d-128">Identifier of the API Release.</span></span>
<span data-ttu-id="38b0d-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="38b0d-129">This parameter is required.</span></span>

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

### <span data-ttu-id="38b0d-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="38b0d-130">-Confirm</span></span>
<span data-ttu-id="38b0d-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b0d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38b0d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38b0d-132">-WhatIf</span></span>
<span data-ttu-id="38b0d-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38b0d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38b0d-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="38b0d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38b0d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b0d-135">CommonParameters</span></span>
<span data-ttu-id="38b0d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38b0d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b0d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b0d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b0d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38b0d-138">INPUTS</span></span>

### <span data-ttu-id="38b0d-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="38b0d-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="38b0d-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="38b0d-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="38b0d-141">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="38b0d-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="38b0d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="38b0d-142">System.String</span></span>

## <span data-ttu-id="38b0d-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38b0d-143">OUTPUTS</span></span>

### <span data-ttu-id="38b0d-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38b0d-144">System.Boolean</span></span>

## <span data-ttu-id="38b0d-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38b0d-145">NOTES</span></span>

## <span data-ttu-id="38b0d-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38b0d-146">RELATED LINKS</span></span>

[<span data-ttu-id="38b0d-147">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="38b0d-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="38b0d-148">Nowe — AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="38b0d-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="38b0d-149">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="38b0d-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
