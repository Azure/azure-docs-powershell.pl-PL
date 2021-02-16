---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: a95be9f18c00d72afb6117d1689f62a6bad053b4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398686"
---
# <span data-ttu-id="d0e83-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="d0e83-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="d0e83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0e83-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e83-103">Usuwa jednostkę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d0e83-103">Removes the cache entity.</span></span>

## <span data-ttu-id="d0e83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0e83-104">SYNTAX</span></span>

### <span data-ttu-id="d0e83-105">ContextParameterSetName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d0e83-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e83-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e83-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e83-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0e83-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0e83-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0e83-108">DESCRIPTION</span></span>
<span data-ttu-id="d0e83-109">Polecenie cmdlet **Remove-AzApiManagementCache** usuwa jednostkę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d0e83-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="d0e83-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0e83-110">EXAMPLES</span></span>

### <span data-ttu-id="d0e83-111">Przykład 1. Usuwanie jednostki pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="d0e83-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="d0e83-112">To polecenie cmdlet usuwa pamięć podręczną `centralus` z usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="d0e83-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="d0e83-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0e83-113">PARAMETERS</span></span>

### <span data-ttu-id="d0e83-114">- CacheId</span><span class="sxs-lookup"><span data-stu-id="d0e83-114">-CacheId</span></span>
<span data-ttu-id="d0e83-115">Identyfikator istniejącego identyfikatora pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="d0e83-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="d0e83-116">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d0e83-116">This parameter is required.</span></span>

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

### <span data-ttu-id="d0e83-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d0e83-117">-Context</span></span>
<span data-ttu-id="d0e83-118">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d0e83-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d0e83-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d0e83-119">This parameter is required.</span></span>

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

### <span data-ttu-id="d0e83-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e83-120">-DefaultProfile</span></span>
<span data-ttu-id="d0e83-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0e83-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0e83-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d0e83-122">-InputObject</span></span>
<span data-ttu-id="d0e83-123">Wystąpienie usługi PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="d0e83-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="d0e83-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d0e83-124">This parameter is required.</span></span>

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

### <span data-ttu-id="d0e83-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0e83-125">-PassThru</span></span>
<span data-ttu-id="d0e83-126">Jeśli zostanie określona, w przypadku gdy operacja zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d0e83-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="d0e83-127">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d0e83-127">This parameter is optional.</span></span>
<span data-ttu-id="d0e83-128">Wartość domyślna to fałsz.</span><span class="sxs-lookup"><span data-stu-id="d0e83-128">Default value is false.</span></span>

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

### <span data-ttu-id="d0e83-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0e83-129">-ResourceId</span></span>
<span data-ttu-id="d0e83-130">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="d0e83-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="d0e83-131">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d0e83-131">This parameter is required.</span></span>

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

### <span data-ttu-id="d0e83-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0e83-132">-Confirm</span></span>
<span data-ttu-id="d0e83-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d0e83-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e83-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0e83-134">-WhatIf</span></span>
<span data-ttu-id="d0e83-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0e83-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e83-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d0e83-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e83-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e83-137">CommonParameters</span></span>
<span data-ttu-id="d0e83-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e83-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e83-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0e83-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e83-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0e83-140">INPUTS</span></span>

### <span data-ttu-id="d0e83-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d0e83-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d0e83-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d0e83-142">System.String</span></span>

### <span data-ttu-id="d0e83-143">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d0e83-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d0e83-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0e83-144">OUTPUTS</span></span>

### <span data-ttu-id="d0e83-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0e83-145">System.Boolean</span></span>

## <span data-ttu-id="d0e83-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0e83-146">NOTES</span></span>

## <span data-ttu-id="d0e83-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0e83-147">RELATED LINKS</span></span>

[<span data-ttu-id="d0e83-148">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="d0e83-148">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="d0e83-149">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="d0e83-149">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="d0e83-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="d0e83-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
