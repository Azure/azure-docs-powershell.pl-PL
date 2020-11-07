---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716464"
---
# <span data-ttu-id="1d4cb-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1d4cb-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="1d4cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d4cb-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4cb-103">Usuwa określoną wersję interfejsu API</span><span class="sxs-lookup"><span data-stu-id="1d4cb-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d4cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d4cb-104">SYNTAX</span></span>

### <span data-ttu-id="1d4cb-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1d4cb-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d4cb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d4cb-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d4cb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1d4cb-107">DESCRIPTION</span></span>

<span data-ttu-id="1d4cb-108">Polecenie cmdlet **Remove-AzureRmApiManagementApiVersionSet** umożliwia usunięcie zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="1d4cb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d4cb-109">EXAMPLES</span></span>

### <span data-ttu-id="1d4cb-110">Przykład 1: usuwanie zestawu wersji interfejsu API</span><span class="sxs-lookup"><span data-stu-id="1d4cb-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="1d4cb-111">To polecenie usuwa zestaw wersji interfejsu API z określonym ApiVersionSetId.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="1d4cb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d4cb-112">PARAMETERS</span></span>

### <span data-ttu-id="1d4cb-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="1d4cb-113">-ApiVersionSetId</span></span>
<span data-ttu-id="1d4cb-114">Identyfikator zestawu wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="1d4cb-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-115">This parameter is required.</span></span>

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

### <span data-ttu-id="1d4cb-116">-Context</span><span class="sxs-lookup"><span data-stu-id="1d4cb-116">-Context</span></span>
<span data-ttu-id="1d4cb-117">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="1d4cb-118">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-118">This parameter is required.</span></span>

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

### <span data-ttu-id="1d4cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4cb-119">-DefaultProfile</span></span>
<span data-ttu-id="1d4cb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d4cb-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1d4cb-121">-InputObject</span></span>
<span data-ttu-id="1d4cb-122">Wystąpienie PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="1d4cb-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-123">This parameter is required.</span></span>

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

### <span data-ttu-id="1d4cb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d4cb-124">-PassThru</span></span>
<span data-ttu-id="1d4cb-125">Jeśli ta wartość zostanie określona, operacja ta zostanie zapisana jako prawda w przypadku powodzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="1d4cb-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="1d4cb-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d4cb-127">-Confirm</span></span>
<span data-ttu-id="1d4cb-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d4cb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d4cb-129">-WhatIf</span></span>
<span data-ttu-id="1d4cb-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d4cb-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d4cb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4cb-132">CommonParameters</span></span>
<span data-ttu-id="1d4cb-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d4cb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4cb-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d4cb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4cb-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d4cb-135">INPUTS</span></span>

### <span data-ttu-id="1d4cb-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1d4cb-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="1d4cb-137">Parametry: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d4cb-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="1d4cb-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1d4cb-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="1d4cb-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1d4cb-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="1d4cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="1d4cb-140">System.String</span></span>

## <span data-ttu-id="1d4cb-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d4cb-141">OUTPUTS</span></span>

### <span data-ttu-id="1d4cb-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d4cb-142">System.Boolean</span></span>

## <span data-ttu-id="1d4cb-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d4cb-143">NOTES</span></span>

## <span data-ttu-id="1d4cb-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d4cb-144">RELATED LINKS</span></span>

[<span data-ttu-id="1d4cb-145">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1d4cb-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="1d4cb-146">Nowe — AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1d4cb-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="1d4cb-147">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="1d4cb-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
