---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 03092cf9577bb7b8a35fd0ef69f5d3c94e9c92de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706965"
---
# <span data-ttu-id="12c5e-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="12c5e-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="12c5e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12c5e-102">SYNOPSIS</span></span>
<span data-ttu-id="12c5e-103">Usuwa określoną wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="12c5e-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="12c5e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12c5e-104">SYNTAX</span></span>

### <span data-ttu-id="12c5e-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="12c5e-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12c5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="12c5e-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12c5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="12c5e-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12c5e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="12c5e-108">DESCRIPTION</span></span>

<span data-ttu-id="12c5e-109">Polecenie cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** umożliwia usunięcie zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="12c5e-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="12c5e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12c5e-110">EXAMPLES</span></span>

### <span data-ttu-id="12c5e-111">Przykład 1: usuwanie zestawu wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="12c5e-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="12c5e-112">To polecenie usuwa zestaw wersji interfejsu API z określonym ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="12c5e-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="12c5e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12c5e-113">PARAMETERS</span></span>

### <span data-ttu-id="12c5e-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="12c5e-114">-ApiVersionSetId</span></span>
<span data-ttu-id="12c5e-115">Identyfikator zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="12c5e-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="12c5e-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="12c5e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="12c5e-117">-Context</span><span class="sxs-lookup"><span data-stu-id="12c5e-117">-Context</span></span>
<span data-ttu-id="12c5e-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="12c5e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="12c5e-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="12c5e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="12c5e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12c5e-120">-DefaultProfile</span></span>
<span data-ttu-id="12c5e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12c5e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12c5e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12c5e-122">-InputObject</span></span>
<span data-ttu-id="12c5e-123">Wystąpienie PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="12c5e-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="12c5e-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="12c5e-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12c5e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12c5e-125">-PassThru</span></span>
<span data-ttu-id="12c5e-126">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="12c5e-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="12c5e-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="12c5e-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="12c5e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12c5e-128">-ResourceId</span></span>
<span data-ttu-id="12c5e-129">Identyfikator zasobu ARM ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="12c5e-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="12c5e-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="12c5e-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12c5e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12c5e-131">-Confirm</span></span>
<span data-ttu-id="12c5e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12c5e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12c5e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12c5e-133">-WhatIf</span></span>
<span data-ttu-id="12c5e-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12c5e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12c5e-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12c5e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12c5e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12c5e-136">CommonParameters</span></span>
<span data-ttu-id="12c5e-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12c5e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12c5e-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12c5e-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12c5e-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12c5e-139">INPUTS</span></span>

### <span data-ttu-id="12c5e-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="12c5e-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="12c5e-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="12c5e-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="12c5e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="12c5e-142">System.String</span></span>

## <span data-ttu-id="12c5e-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12c5e-143">OUTPUTS</span></span>

### <span data-ttu-id="12c5e-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12c5e-144">System.Boolean</span></span>

## <span data-ttu-id="12c5e-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12c5e-145">NOTES</span></span>

## <span data-ttu-id="12c5e-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12c5e-146">RELATED LINKS</span></span>

[<span data-ttu-id="12c5e-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="12c5e-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="12c5e-148">Nowe — AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="12c5e-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="12c5e-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="12c5e-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)