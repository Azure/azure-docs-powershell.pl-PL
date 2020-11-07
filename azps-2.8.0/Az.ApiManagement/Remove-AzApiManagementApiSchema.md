---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: 4fa05a0c3568d8d787a7b269cd0f26c0adc82d0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706966"
---
# <span data-ttu-id="7107c-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7107c-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="7107c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7107c-102">SYNOPSIS</span></span>
<span data-ttu-id="7107c-103">Usuwa schemat API z interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7107c-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="7107c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7107c-104">SYNTAX</span></span>

### <span data-ttu-id="7107c-105">ByApiSchemaId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7107c-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7107c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7107c-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7107c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7107c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7107c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7107c-108">DESCRIPTION</span></span>
<span data-ttu-id="7107c-109">Polecenie cmdlet **Remove-AzApiManagementSchema** z interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7107c-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="7107c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7107c-110">EXAMPLES</span></span>

### <span data-ttu-id="7107c-111">Przykład 1: Usunięcie schematu API z interfejsu API</span><span class="sxs-lookup"><span data-stu-id="7107c-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="7107c-112">Skrypt usuwa schemat `2` z interfejsu API, `echo-api` Jeśli nie ma do niego odwołania.</span><span class="sxs-lookup"><span data-stu-id="7107c-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="7107c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7107c-113">PARAMETERS</span></span>

### <span data-ttu-id="7107c-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="7107c-114">-ApiId</span></span>
<span data-ttu-id="7107c-115">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7107c-115">Identifier of the API.</span></span>
<span data-ttu-id="7107c-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7107c-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7107c-117">-Context</span><span class="sxs-lookup"><span data-stu-id="7107c-117">-Context</span></span>
<span data-ttu-id="7107c-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7107c-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="7107c-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7107c-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7107c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7107c-120">-DefaultProfile</span></span>
<span data-ttu-id="7107c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7107c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7107c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7107c-122">-InputObject</span></span>
<span data-ttu-id="7107c-123">Wystąpienie PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="7107c-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="7107c-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7107c-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7107c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7107c-125">-PassThru</span></span>
<span data-ttu-id="7107c-126">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="7107c-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="7107c-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7107c-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="7107c-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7107c-128">-ResourceId</span></span>
<span data-ttu-id="7107c-129">Identyfikator zasobu ARM ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="7107c-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="7107c-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7107c-130">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7107c-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="7107c-131">-SchemaId</span></span>
<span data-ttu-id="7107c-132">Identyfikator schematu API.</span><span class="sxs-lookup"><span data-stu-id="7107c-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="7107c-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="7107c-133">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiSchemaId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7107c-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7107c-134">-Confirm</span></span>
<span data-ttu-id="7107c-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7107c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7107c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7107c-136">-WhatIf</span></span>
<span data-ttu-id="7107c-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7107c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7107c-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7107c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7107c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7107c-139">CommonParameters</span></span>
<span data-ttu-id="7107c-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7107c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7107c-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7107c-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7107c-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7107c-142">INPUTS</span></span>

### <span data-ttu-id="7107c-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="7107c-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="7107c-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7107c-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="7107c-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7107c-145">System.String</span></span>

## <span data-ttu-id="7107c-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7107c-146">OUTPUTS</span></span>

### <span data-ttu-id="7107c-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7107c-147">System.Boolean</span></span>

## <span data-ttu-id="7107c-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7107c-148">NOTES</span></span>

## <span data-ttu-id="7107c-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7107c-149">RELATED LINKS</span></span>

[<span data-ttu-id="7107c-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7107c-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="7107c-151">Nowe — AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7107c-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="7107c-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="7107c-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
