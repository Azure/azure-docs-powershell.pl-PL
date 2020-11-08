---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232353"
---
# <span data-ttu-id="65990-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="65990-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="65990-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65990-102">SYNOPSIS</span></span>
<span data-ttu-id="65990-103">Tworzy nowy schemat interfejsu API w usłudze ApiManagement</span><span class="sxs-lookup"><span data-stu-id="65990-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="65990-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65990-104">SYNTAX</span></span>

### <span data-ttu-id="65990-105">SchemaDocumentInline (domyślny)</span><span class="sxs-lookup"><span data-stu-id="65990-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="65990-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="65990-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65990-107">Opis</span><span class="sxs-lookup"><span data-stu-id="65990-107">DESCRIPTION</span></span>
<span data-ttu-id="65990-108">Tworzy nowy schemat API interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="65990-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="65990-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65990-109">EXAMPLES</span></span>

### <span data-ttu-id="65990-110">Przykład 1: Tworzenie nowego schematu dla wszechstronnego interfejsu API struktury Swagger petstore</span><span class="sxs-lookup"><span data-stu-id="65990-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="65990-111">Polecenie cmdlet **New-AzApiManagementApiSchema** umożliwia utworzenie lub zaktualizowanie schematu `swagger-petstore-extensive` interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="65990-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="65990-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65990-112">PARAMETERS</span></span>

### <span data-ttu-id="65990-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="65990-113">-ApiId</span></span>
<span data-ttu-id="65990-114">Identyfikator API.</span><span class="sxs-lookup"><span data-stu-id="65990-114">Identifier of api.</span></span> <span data-ttu-id="65990-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="65990-115">This parameter is required.</span></span>

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

### <span data-ttu-id="65990-116">-Context</span><span class="sxs-lookup"><span data-stu-id="65990-116">-Context</span></span>
<span data-ttu-id="65990-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="65990-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="65990-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="65990-118">This parameter is required.</span></span>

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

### <span data-ttu-id="65990-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65990-119">-DefaultProfile</span></span>
<span data-ttu-id="65990-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65990-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65990-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="65990-121">-SchemaDocument</span></span>
<span data-ttu-id="65990-122">Dokument schematu API jako ciąg.</span><span class="sxs-lookup"><span data-stu-id="65990-122">Api schema document as a string.</span></span> <span data-ttu-id="65990-123">Ten parametr jest wymagany — SchemaDocumentFile nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="65990-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="65990-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="65990-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="65990-125">ContentType schematu API.</span><span class="sxs-lookup"><span data-stu-id="65990-125">ContentType of the api Schema.</span></span> <span data-ttu-id="65990-126">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="65990-126">This parameter is required.</span></span>

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

### <span data-ttu-id="65990-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="65990-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="65990-128">Ścieżka pliku dokumentu schematu API.</span><span class="sxs-lookup"><span data-stu-id="65990-128">Api schema document file path.</span></span> <span data-ttu-id="65990-129">Ten parametr jest wymagany — SchemaDocument nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="65990-129">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="65990-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="65990-130">-SchemaId</span></span>
<span data-ttu-id="65990-131">Identyfikator nowego schematu.</span><span class="sxs-lookup"><span data-stu-id="65990-131">Identifier of new schema.</span></span>
<span data-ttu-id="65990-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="65990-132">This parameter is optional.</span></span>
<span data-ttu-id="65990-133">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="65990-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="65990-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65990-134">-Confirm</span></span>
<span data-ttu-id="65990-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65990-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65990-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65990-136">-WhatIf</span></span>
<span data-ttu-id="65990-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65990-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65990-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65990-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65990-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65990-139">CommonParameters</span></span>
<span data-ttu-id="65990-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65990-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65990-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65990-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65990-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65990-142">INPUTS</span></span>

### <span data-ttu-id="65990-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="65990-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="65990-144">System. String</span><span class="sxs-lookup"><span data-stu-id="65990-144">System.String</span></span>

## <span data-ttu-id="65990-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65990-145">OUTPUTS</span></span>

### <span data-ttu-id="65990-146">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="65990-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="65990-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65990-147">NOTES</span></span>

## <span data-ttu-id="65990-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65990-148">RELATED LINKS</span></span>

[<span data-ttu-id="65990-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="65990-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="65990-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="65990-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="65990-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="65990-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
