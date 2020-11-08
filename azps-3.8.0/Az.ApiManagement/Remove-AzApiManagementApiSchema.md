---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiSchema.md
ms.openlocfilehash: fb144bfa228b07501c374f054970d1e3e0337ec1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94054035"
---
# <span data-ttu-id="5acb5-101">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="5acb5-101">Remove-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="5acb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5acb5-102">SYNOPSIS</span></span>
<span data-ttu-id="5acb5-103">Usuwa schemat API z interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5acb5-103">Removes the API Schema from the API.</span></span>

## <span data-ttu-id="5acb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5acb5-104">SYNTAX</span></span>

### <span data-ttu-id="5acb5-105">ByApiSchemaId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5acb5-105">ByApiSchemaId (Default)</span></span>
```
Remove-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5acb5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5acb5-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5acb5-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5acb5-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementApiSchema -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5acb5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5acb5-108">DESCRIPTION</span></span>
<span data-ttu-id="5acb5-109">Polecenie cmdlet **Remove-AzApiManagementSchema** z interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5acb5-109">The cmdlet **Remove-AzApiManagementSchema** from the Api.</span></span>

## <span data-ttu-id="5acb5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5acb5-110">EXAMPLES</span></span>

### <span data-ttu-id="5acb5-111">Przykład 1: Usunięcie schematu API z interfejsu API</span><span class="sxs-lookup"><span data-stu-id="5acb5-111">Example 1 : Removes the Api Schema from the API</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiSchema -Context $apimContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="5acb5-112">Skrypt usuwa schemat `2` z interfejsu API, `echo-api` Jeśli nie ma do niego odwołania.</span><span class="sxs-lookup"><span data-stu-id="5acb5-112">The script removes the Schema `2` from the Api `echo-api` if it is not referenced.</span></span>

## <span data-ttu-id="5acb5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5acb5-113">PARAMETERS</span></span>

### <span data-ttu-id="5acb5-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5acb5-114">-ApiId</span></span>
<span data-ttu-id="5acb5-115">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="5acb5-115">Identifier of the API.</span></span>
<span data-ttu-id="5acb5-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5acb5-116">This parameter is required.</span></span>

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

### <span data-ttu-id="5acb5-117">-Context</span><span class="sxs-lookup"><span data-stu-id="5acb5-117">-Context</span></span>
<span data-ttu-id="5acb5-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="5acb5-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="5acb5-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5acb5-119">This parameter is required.</span></span>

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

### <span data-ttu-id="5acb5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5acb5-120">-DefaultProfile</span></span>
<span data-ttu-id="5acb5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5acb5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5acb5-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5acb5-122">-InputObject</span></span>
<span data-ttu-id="5acb5-123">Wystąpienie PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="5acb5-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="5acb5-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5acb5-124">This parameter is required.</span></span>

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

### <span data-ttu-id="5acb5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5acb5-125">-PassThru</span></span>
<span data-ttu-id="5acb5-126">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="5acb5-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="5acb5-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="5acb5-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="5acb5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5acb5-128">-ResourceId</span></span>
<span data-ttu-id="5acb5-129">Identyfikator zasobu ARM ApiSchema.</span><span class="sxs-lookup"><span data-stu-id="5acb5-129">Arm ResourceId of ApiSchema.</span></span> <span data-ttu-id="5acb5-130">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5acb5-130">This parameter is required.</span></span>

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

### <span data-ttu-id="5acb5-131">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="5acb5-131">-SchemaId</span></span>
<span data-ttu-id="5acb5-132">Identyfikator schematu API.</span><span class="sxs-lookup"><span data-stu-id="5acb5-132">Identifier of the API Schema.</span></span>
<span data-ttu-id="5acb5-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="5acb5-133">This parameter is required.</span></span>

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

### <span data-ttu-id="5acb5-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5acb5-134">-Confirm</span></span>
<span data-ttu-id="5acb5-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5acb5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5acb5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5acb5-136">-WhatIf</span></span>
<span data-ttu-id="5acb5-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5acb5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5acb5-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5acb5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5acb5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5acb5-139">CommonParameters</span></span>
<span data-ttu-id="5acb5-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5acb5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5acb5-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5acb5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5acb5-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5acb5-142">INPUTS</span></span>

### <span data-ttu-id="5acb5-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5acb5-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5acb5-144">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="5acb5-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="5acb5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="5acb5-145">System.String</span></span>

## <span data-ttu-id="5acb5-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5acb5-146">OUTPUTS</span></span>

### <span data-ttu-id="5acb5-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5acb5-147">System.Boolean</span></span>

## <span data-ttu-id="5acb5-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5acb5-148">NOTES</span></span>

## <span data-ttu-id="5acb5-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5acb5-149">RELATED LINKS</span></span>

[<span data-ttu-id="5acb5-150">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="5acb5-150">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="5acb5-151">Nowe — AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="5acb5-151">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="5acb5-152">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="5acb5-152">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
