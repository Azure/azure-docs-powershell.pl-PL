---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: ffca6c1bc32d809f7bbb93c3b76dd9490f9fafb8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178091"
---
# <span data-ttu-id="abd18-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="abd18-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="abd18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abd18-102">SYNOPSIS</span></span>
<span data-ttu-id="abd18-103">Usuwa jednostkę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="abd18-103">Removes the cache entity.</span></span>

## <span data-ttu-id="abd18-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="abd18-104">SYNTAX</span></span>

### <span data-ttu-id="abd18-105">ContextParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="abd18-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abd18-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="abd18-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="abd18-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="abd18-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abd18-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="abd18-108">DESCRIPTION</span></span>
<span data-ttu-id="abd18-109">Polecenie cmdlet **Remove-AzApiManagementCache** usuwa jednostkę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="abd18-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="abd18-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="abd18-110">EXAMPLES</span></span>

### <span data-ttu-id="abd18-111">Przykład 1. Usuwanie jednostki pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="abd18-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="abd18-112">To polecenie cmdlet usuwa pamięć podręczną `centralus` z usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="abd18-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="abd18-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="abd18-113">PARAMETERS</span></span>

### <span data-ttu-id="abd18-114">- CacheId</span><span class="sxs-lookup"><span data-stu-id="abd18-114">-CacheId</span></span>
<span data-ttu-id="abd18-115">Identyfikator istniejącego identyfikatora pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="abd18-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="abd18-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="abd18-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abd18-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="abd18-117">-Context</span></span>
<span data-ttu-id="abd18-118">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="abd18-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="abd18-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="abd18-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abd18-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abd18-120">-DefaultProfile</span></span>
<span data-ttu-id="abd18-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="abd18-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abd18-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abd18-122">-InputObject</span></span>
<span data-ttu-id="abd18-123">Wystąpienie usługi PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="abd18-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="abd18-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="abd18-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abd18-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abd18-125">-PassThru</span></span>
<span data-ttu-id="abd18-126">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="abd18-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="abd18-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="abd18-127">This parameter is optional.</span></span>
<span data-ttu-id="abd18-128">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="abd18-128">Default value is false.</span></span>

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

### <span data-ttu-id="abd18-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="abd18-129">-ResourceId</span></span>
<span data-ttu-id="abd18-130">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="abd18-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="abd18-131">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="abd18-131">This parameter is required.</span></span>

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

### <span data-ttu-id="abd18-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="abd18-132">-Confirm</span></span>
<span data-ttu-id="abd18-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="abd18-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abd18-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abd18-134">-WhatIf</span></span>
<span data-ttu-id="abd18-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abd18-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abd18-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="abd18-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abd18-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abd18-137">CommonParameters</span></span>
<span data-ttu-id="abd18-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abd18-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abd18-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abd18-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abd18-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abd18-140">INPUTS</span></span>

### <span data-ttu-id="abd18-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="abd18-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="abd18-142">System.String</span><span class="sxs-lookup"><span data-stu-id="abd18-142">System.String</span></span>

### <span data-ttu-id="abd18-143">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="abd18-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="abd18-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abd18-144">OUTPUTS</span></span>

### <span data-ttu-id="abd18-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="abd18-145">System.Boolean</span></span>

## <span data-ttu-id="abd18-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="abd18-146">NOTES</span></span>

## <span data-ttu-id="abd18-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abd18-147">RELATED LINKS</span></span>

[<span data-ttu-id="abd18-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="abd18-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="abd18-149">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="abd18-149">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="abd18-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="abd18-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
