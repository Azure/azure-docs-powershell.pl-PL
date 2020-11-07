---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 02091c1a207bc10fbdb539fb9a301d002b631827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706915"
---
# <span data-ttu-id="8d9e1-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8d9e1-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="8d9e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8d9e1-102">SYNOPSIS</span></span>
<span data-ttu-id="8d9e1-103">Modyfikuje schemat API</span><span class="sxs-lookup"><span data-stu-id="8d9e1-103">Modifies an API Schema</span></span>

## <span data-ttu-id="8d9e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8d9e1-104">SYNTAX</span></span>

### <span data-ttu-id="8d9e1-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8d9e1-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d9e1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8d9e1-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d9e1-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d9e1-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d9e1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8d9e1-108">DESCRIPTION</span></span>
<span data-ttu-id="8d9e1-109">Polecenie cmdlet **Set-AzApiManagementApiSchema** modyfikuje schemat interfejsu API zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="8d9e1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8d9e1-110">EXAMPLES</span></span>

### <span data-ttu-id="8d9e1-111">Przykład 1. modyfikuje schemat API</span><span class="sxs-lookup"><span data-stu-id="8d9e1-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="8d9e1-112">W przykładzie Zaktualizowano schemat API</span><span class="sxs-lookup"><span data-stu-id="8d9e1-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="8d9e1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8d9e1-113">PARAMETERS</span></span>

### <span data-ttu-id="8d9e1-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="8d9e1-114">-ApiId</span></span>
<span data-ttu-id="8d9e1-115">Identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-115">Identifier of existing API.</span></span>
<span data-ttu-id="8d9e1-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-116">This parameter is required.</span></span>

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

### <span data-ttu-id="8d9e1-117">-Context</span><span class="sxs-lookup"><span data-stu-id="8d9e1-117">-Context</span></span>
<span data-ttu-id="8d9e1-118">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8d9e1-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-119">This parameter is required.</span></span>

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

### <span data-ttu-id="8d9e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d9e1-120">-DefaultProfile</span></span>
<span data-ttu-id="8d9e1-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d9e1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d9e1-122">-InputObject</span></span>
<span data-ttu-id="8d9e1-123">Wystąpienie PsApiManagementApiSchema.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="8d9e1-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-124">This parameter is required.</span></span>

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

### <span data-ttu-id="8d9e1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d9e1-125">-PassThru</span></span>
<span data-ttu-id="8d9e1-126">Jeśli jest określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementApi reprezentujące zestaw interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e1-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d9e1-127">-ResourceId</span></span>
<span data-ttu-id="8d9e1-128">Identyfikator zasobu ARM dla schematu diagnostycznego lub interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="8d9e1-129">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-129">This parameter is required.</span></span>

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

### <span data-ttu-id="8d9e1-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="8d9e1-130">-SchemaDocument</span></span>
<span data-ttu-id="8d9e1-131">Dokument schematu API jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-131">Api schema document as a string.</span></span> <span data-ttu-id="8d9e1-132">Ten parametr jest wymagany — SchemaDocumentFile nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e1-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="8d9e1-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="8d9e1-134">ContentType schematu API.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-134">ContentType of the api Schema.</span></span> <span data-ttu-id="8d9e1-135">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-135">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e1-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="8d9e1-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="8d9e1-137">Ścieżka pliku dokumentu schematu API.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-137">Api schema document file path.</span></span> <span data-ttu-id="8d9e1-138">Ten parametr jest wymagany — SchemaDocument nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-138">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d9e1-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="8d9e1-139">-SchemaId</span></span>
<span data-ttu-id="8d9e1-140">Identyfikator istniejącego schematu.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="8d9e1-141">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-141">This parameter is required.</span></span>

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

### <span data-ttu-id="8d9e1-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d9e1-142">-Confirm</span></span>
<span data-ttu-id="8d9e1-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d9e1-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d9e1-144">-WhatIf</span></span>
<span data-ttu-id="8d9e1-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d9e1-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d9e1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d9e1-147">CommonParameters</span></span>
<span data-ttu-id="8d9e1-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d9e1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d9e1-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d9e1-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d9e1-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d9e1-150">INPUTS</span></span>

### <span data-ttu-id="8d9e1-151">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8d9e1-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8d9e1-152">System. String</span><span class="sxs-lookup"><span data-stu-id="8d9e1-152">System.String</span></span>

### <span data-ttu-id="8d9e1-153">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8d9e1-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="8d9e1-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8d9e1-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8d9e1-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8d9e1-155">OUTPUTS</span></span>

### <span data-ttu-id="8d9e1-156">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="8d9e1-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="8d9e1-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8d9e1-157">NOTES</span></span>

## <span data-ttu-id="8d9e1-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d9e1-158">RELATED LINKS</span></span>

[<span data-ttu-id="8d9e1-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8d9e1-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="8d9e1-160">Nowe — AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8d9e1-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="8d9e1-161">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="8d9e1-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

