---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 681ce525d1d00802cc226539fd9c3014c1786098
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869455"
---
# <span data-ttu-id="c11bc-101">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c11bc-101">Remove-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="c11bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c11bc-102">SYNOPSIS</span></span>
<span data-ttu-id="c11bc-103">Usuwa określoną wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c11bc-103">Removes a particular Api Version Set</span></span>

## <span data-ttu-id="c11bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c11bc-104">SYNTAX</span></span>

### <span data-ttu-id="c11bc-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c11bc-105">ExpandedParameter (Default)</span></span>
```
Remove-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c11bc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c11bc-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c11bc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c11bc-107">DESCRIPTION</span></span>

<span data-ttu-id="c11bc-108">Polecenie cmdlet **Remove-AzAzureRmApiManagementApiVersionSet** umożliwia usunięcie zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c11bc-108">The **Remove-AzAzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="c11bc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c11bc-109">EXAMPLES</span></span>

### <span data-ttu-id="c11bc-110">Przykład 1: usuwanie zestawu wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="c11bc-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="c11bc-111">To polecenie usuwa zestaw wersji interfejsu API z określonym ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="c11bc-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="c11bc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c11bc-112">PARAMETERS</span></span>

### <span data-ttu-id="c11bc-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="c11bc-113">-ApiVersionSetId</span></span>
<span data-ttu-id="c11bc-114">Identyfikator zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="c11bc-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="c11bc-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c11bc-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c11bc-116">-Context</span><span class="sxs-lookup"><span data-stu-id="c11bc-116">-Context</span></span>
<span data-ttu-id="c11bc-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c11bc-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c11bc-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c11bc-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c11bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11bc-119">-DefaultProfile</span></span>
<span data-ttu-id="c11bc-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c11bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c11bc-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c11bc-121">-InputObject</span></span>
<span data-ttu-id="c11bc-122">Wystąpienie PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="c11bc-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="c11bc-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c11bc-123">This parameter is required.</span></span>

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

### <span data-ttu-id="c11bc-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c11bc-124">-PassThru</span></span>
<span data-ttu-id="c11bc-125">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="c11bc-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="c11bc-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c11bc-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="c11bc-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c11bc-127">-Confirm</span></span>
<span data-ttu-id="c11bc-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c11bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c11bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c11bc-129">-WhatIf</span></span>
<span data-ttu-id="c11bc-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c11bc-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c11bc-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c11bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c11bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11bc-132">CommonParameters</span></span>
<span data-ttu-id="c11bc-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c11bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11bc-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c11bc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11bc-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c11bc-135">INPUTS</span></span>

### <span data-ttu-id="c11bc-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c11bc-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c11bc-137">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c11bc-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="c11bc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c11bc-138">System.String</span></span>

## <span data-ttu-id="c11bc-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c11bc-139">OUTPUTS</span></span>

### <span data-ttu-id="c11bc-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c11bc-140">System.Boolean</span></span>

## <span data-ttu-id="c11bc-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c11bc-141">NOTES</span></span>

## <span data-ttu-id="c11bc-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c11bc-142">RELATED LINKS</span></span>

[<span data-ttu-id="c11bc-143">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c11bc-143">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c11bc-144">Nowe — AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c11bc-144">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="c11bc-145">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="c11bc-145">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)