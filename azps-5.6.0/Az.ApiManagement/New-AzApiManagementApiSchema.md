---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7ac8d0b243f70d9e0f02c620febc7062f0c2e3ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962506"
---
# <span data-ttu-id="b65e4-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="b65e4-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="b65e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b65e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b65e4-103">Tworzy nowy schemat interfejsu API w usłudze ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b65e4-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="b65e4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b65e4-104">SYNTAX</span></span>

### <span data-ttu-id="b65e4-105">SchemaDocumentInline (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b65e4-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b65e4-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="b65e4-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b65e4-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b65e4-107">DESCRIPTION</span></span>
<span data-ttu-id="b65e4-108">Tworzy nowy schemat interfejsu API interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b65e4-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="b65e4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b65e4-109">EXAMPLES</span></span>

### <span data-ttu-id="b65e4-110">Przykład 1. Tworzenie nowego schematu dla rozległego interfejsu API Swagger Petstore</span><span class="sxs-lookup"><span data-stu-id="b65e4-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="b65e4-111">Polecenie cmdlet **New-AzApiManagementApiSchema** tworzy lub aktualizuje schemat `swagger-petstore-extensive` aPI.</span><span class="sxs-lookup"><span data-stu-id="b65e4-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="b65e4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b65e4-112">PARAMETERS</span></span>

### <span data-ttu-id="b65e4-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b65e4-113">-ApiId</span></span>
<span data-ttu-id="b65e4-114">Identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b65e4-114">Identifier of api.</span></span> <span data-ttu-id="b65e4-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b65e4-115">This parameter is required.</span></span>

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

### <span data-ttu-id="b65e4-116">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b65e4-116">-Context</span></span>
<span data-ttu-id="b65e4-117">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b65e4-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b65e4-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b65e4-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b65e4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65e4-119">-DefaultProfile</span></span>
<span data-ttu-id="b65e4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b65e4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b65e4-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="b65e4-121">-SchemaDocument</span></span>
<span data-ttu-id="b65e4-122">Dokument schematu interfejsu API jako ciąg znaków.</span><span class="sxs-lookup"><span data-stu-id="b65e4-122">Api schema document as a string.</span></span> <span data-ttu-id="b65e4-123">Ten parametr jest wymagany. Nie określono parametru SchemaDocumentFile.</span><span class="sxs-lookup"><span data-stu-id="b65e4-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65e4-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="b65e4-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="b65e4-125">ContentType schematu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b65e4-125">ContentType of the api Schema.</span></span> <span data-ttu-id="b65e4-126">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b65e4-126">This parameter is required.</span></span>

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

### <span data-ttu-id="b65e4-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="b65e4-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="b65e4-128">Ścieżka pliku dokumentu schematu interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b65e4-128">Api schema document file path.</span></span> <span data-ttu-id="b65e4-129">Ten parametr jest wymagany. Nie określono parametru SchemaDocument.</span><span class="sxs-lookup"><span data-stu-id="b65e4-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65e4-130">- SchemaId</span><span class="sxs-lookup"><span data-stu-id="b65e4-130">-SchemaId</span></span>
<span data-ttu-id="b65e4-131">Identyfikator nowego schematu.</span><span class="sxs-lookup"><span data-stu-id="b65e4-131">Identifier of new schema.</span></span>
<span data-ttu-id="b65e4-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b65e4-132">This parameter is optional.</span></span>
<span data-ttu-id="b65e4-133">Jeśli nie określono, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="b65e4-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="b65e4-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b65e4-134">-Confirm</span></span>
<span data-ttu-id="b65e4-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b65e4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b65e4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b65e4-136">-WhatIf</span></span>
<span data-ttu-id="b65e4-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b65e4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b65e4-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b65e4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b65e4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65e4-139">CommonParameters</span></span>
<span data-ttu-id="b65e4-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b65e4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65e4-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b65e4-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65e4-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b65e4-142">INPUTS</span></span>

### <span data-ttu-id="b65e4-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b65e4-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b65e4-144">System.String</span><span class="sxs-lookup"><span data-stu-id="b65e4-144">System.String</span></span>

## <span data-ttu-id="b65e4-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b65e4-145">OUTPUTS</span></span>

### <span data-ttu-id="b65e4-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="b65e4-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="b65e4-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b65e4-147">NOTES</span></span>

## <span data-ttu-id="b65e4-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b65e4-148">RELATED LINKS</span></span>

[<span data-ttu-id="b65e4-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="b65e4-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="b65e4-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="b65e4-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="b65e4-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="b65e4-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
