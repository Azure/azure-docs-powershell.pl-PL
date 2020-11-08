---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 58a082288a121e5e6b04353bad862edaea4c20fc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232337"
---
# <span data-ttu-id="08f55-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08f55-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="08f55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08f55-102">SYNOPSIS</span></span>
<span data-ttu-id="08f55-103">Usuwa określoną wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="08f55-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="08f55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08f55-104">SYNTAX</span></span>

### <span data-ttu-id="08f55-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="08f55-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f55-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="08f55-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08f55-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="08f55-107">ByResourceId</span></span>
```
Remove-AzApiManagementApiVersionSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08f55-108">Opis</span><span class="sxs-lookup"><span data-stu-id="08f55-108">DESCRIPTION</span></span>

<span data-ttu-id="08f55-109">Polecenie cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** umożliwia usunięcie zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="08f55-109">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="08f55-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08f55-110">EXAMPLES</span></span>

### <span data-ttu-id="08f55-111">Przykład 1: usuwanie zestawu wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="08f55-111">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="08f55-112">To polecenie usuwa zestaw wersji interfejsu API z określonym ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="08f55-112">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="08f55-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08f55-113">PARAMETERS</span></span>

### <span data-ttu-id="08f55-114">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="08f55-114">-ApiVersionSetId</span></span>
<span data-ttu-id="08f55-115">Identyfikator zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="08f55-115">Identifier of the API Version Set.</span></span>
<span data-ttu-id="08f55-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="08f55-116">This parameter is required.</span></span>

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

### <span data-ttu-id="08f55-117">-Context</span><span class="sxs-lookup"><span data-stu-id="08f55-117">-Context</span></span>
<span data-ttu-id="08f55-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="08f55-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="08f55-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="08f55-119">This parameter is required.</span></span>

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

### <span data-ttu-id="08f55-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08f55-120">-DefaultProfile</span></span>
<span data-ttu-id="08f55-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08f55-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08f55-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="08f55-122">-InputObject</span></span>
<span data-ttu-id="08f55-123">Wystąpienie PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="08f55-123">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="08f55-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="08f55-124">This parameter is required.</span></span>

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

### <span data-ttu-id="08f55-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08f55-125">-PassThru</span></span>
<span data-ttu-id="08f55-126">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="08f55-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="08f55-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="08f55-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="08f55-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08f55-128">-ResourceId</span></span>
<span data-ttu-id="08f55-129">Identyfikator zasobu ARM ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="08f55-129">Arm ResourceId of ApiVersionSet.</span></span> <span data-ttu-id="08f55-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="08f55-130">This parameter is required.</span></span>

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

### <span data-ttu-id="08f55-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08f55-131">-Confirm</span></span>
<span data-ttu-id="08f55-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08f55-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08f55-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08f55-133">-WhatIf</span></span>
<span data-ttu-id="08f55-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08f55-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08f55-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08f55-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08f55-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08f55-136">CommonParameters</span></span>
<span data-ttu-id="08f55-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08f55-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08f55-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08f55-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08f55-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08f55-139">INPUTS</span></span>

### <span data-ttu-id="08f55-140">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="08f55-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="08f55-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08f55-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="08f55-142">System. String</span><span class="sxs-lookup"><span data-stu-id="08f55-142">System.String</span></span>

## <span data-ttu-id="08f55-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08f55-143">OUTPUTS</span></span>

### <span data-ttu-id="08f55-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08f55-144">System.Boolean</span></span>

## <span data-ttu-id="08f55-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08f55-145">NOTES</span></span>

## <span data-ttu-id="08f55-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08f55-146">RELATED LINKS</span></span>

[<span data-ttu-id="08f55-147">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08f55-147">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="08f55-148">Nowe — AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08f55-148">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="08f55-149">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="08f55-149">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)