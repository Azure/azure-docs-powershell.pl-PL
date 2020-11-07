---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 31e2151e5c41a4e4c9d053174f9d598cd16680f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706969"
---
# <span data-ttu-id="04d46-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04d46-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="04d46-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04d46-102">SYNOPSIS</span></span>
<span data-ttu-id="04d46-103">Usuwa określoną wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="04d46-103">Removes a particular API Release</span></span>

## <span data-ttu-id="04d46-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04d46-104">SYNTAX</span></span>

### <span data-ttu-id="04d46-105">ByApiReleaseId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="04d46-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04d46-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="04d46-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d46-107">Opis</span><span class="sxs-lookup"><span data-stu-id="04d46-107">DESCRIPTION</span></span>

<span data-ttu-id="04d46-108">Polecenie cmdlet **Remove-AzAzureRmApiManagementApiRelease** Usuwa istniejącą wersję interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="04d46-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="04d46-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04d46-109">EXAMPLES</span></span>

### <span data-ttu-id="04d46-110">Przykład 1: Usuwanie wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="04d46-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="04d46-111">To polecenie powoduje usunięcie wersji interfejsu API z określonym ApiId i ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="04d46-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="04d46-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04d46-112">PARAMETERS</span></span>

### <span data-ttu-id="04d46-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="04d46-113">-ApiId</span></span>
<span data-ttu-id="04d46-114">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="04d46-114">Identifier of the API.</span></span>
<span data-ttu-id="04d46-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="04d46-115">This parameter is required.</span></span>

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

### <span data-ttu-id="04d46-116">-Context</span><span class="sxs-lookup"><span data-stu-id="04d46-116">-Context</span></span>
<span data-ttu-id="04d46-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="04d46-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="04d46-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="04d46-118">This parameter is required.</span></span>

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

### <span data-ttu-id="04d46-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d46-119">-DefaultProfile</span></span>
<span data-ttu-id="04d46-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04d46-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04d46-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="04d46-121">-InputObject</span></span>
<span data-ttu-id="04d46-122">Wystąpienie PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="04d46-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="04d46-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="04d46-123">This parameter is required.</span></span>

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

### <span data-ttu-id="04d46-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04d46-124">-PassThru</span></span>
<span data-ttu-id="04d46-125">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="04d46-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="04d46-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="04d46-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="04d46-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="04d46-127">-ReleaseId</span></span>
<span data-ttu-id="04d46-128">Identyfikator wersji API.</span><span class="sxs-lookup"><span data-stu-id="04d46-128">Identifier of the API Release.</span></span>
<span data-ttu-id="04d46-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="04d46-129">This parameter is required.</span></span>

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

### <span data-ttu-id="04d46-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="04d46-130">-Confirm</span></span>
<span data-ttu-id="04d46-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04d46-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d46-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d46-132">-WhatIf</span></span>
<span data-ttu-id="04d46-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04d46-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d46-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="04d46-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d46-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d46-135">CommonParameters</span></span>
<span data-ttu-id="04d46-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04d46-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d46-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="04d46-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d46-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04d46-138">INPUTS</span></span>

### <span data-ttu-id="04d46-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="04d46-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="04d46-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04d46-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="04d46-141">System. String</span><span class="sxs-lookup"><span data-stu-id="04d46-141">System.String</span></span>

## <span data-ttu-id="04d46-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04d46-142">OUTPUTS</span></span>

### <span data-ttu-id="04d46-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="04d46-143">System.Boolean</span></span>

## <span data-ttu-id="04d46-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04d46-144">NOTES</span></span>

## <span data-ttu-id="04d46-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04d46-145">RELATED LINKS</span></span>

[<span data-ttu-id="04d46-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04d46-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="04d46-147">Nowe — AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04d46-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="04d46-148">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="04d46-148">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)