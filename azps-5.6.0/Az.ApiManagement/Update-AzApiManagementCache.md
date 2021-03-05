---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 8c7b423090de10ea1573d268dcc3c301ec4b206d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001946"
---
# <span data-ttu-id="fbe5e-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fbe5e-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="fbe5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbe5e-102">SYNOPSIS</span></span>
<span data-ttu-id="fbe5e-103">aktualizuje pamięć podręczną w usłudze zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="fbe5e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbe5e-104">SYNTAX</span></span>

### <span data-ttu-id="fbe5e-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="fbe5e-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fbe5e-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbe5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbe5e-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbe5e-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbe5e-108">DESCRIPTION</span></span>
<span data-ttu-id="fbe5e-109">Polecenie cmdlet **Update-AzApiManagementCache** aktualizuje pamięć podręczną w usłudze ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="fbe5e-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbe5e-110">EXAMPLES</span></span>

### <span data-ttu-id="fbe5e-111">Przykład 1. Aktualizacja opisu pamięci podręcznej w centralu</span><span class="sxs-lookup"><span data-stu-id="fbe5e-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="fbe5e-112">Aktualizuje opis pamięci podręcznej w centralnym Polsce.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="fbe5e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbe5e-113">PARAMETERS</span></span>

### <span data-ttu-id="fbe5e-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="fbe5e-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="fbe5e-115">Arm ResourceId wystąpienia usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="fbe5e-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbe5e-117">- CacheId</span><span class="sxs-lookup"><span data-stu-id="fbe5e-117">-CacheId</span></span>
<span data-ttu-id="fbe5e-118">Identyfikator nowej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-118">Identifier of new cache.</span></span>
<span data-ttu-id="fbe5e-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-119">This parameter is required.</span></span>

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

### <span data-ttu-id="fbe5e-120">- ConnectionString</span><span class="sxs-lookup"><span data-stu-id="fbe5e-120">-ConnectionString</span></span>
<span data-ttu-id="fbe5e-121">Redis Connection String (Redis Connection String).</span><span class="sxs-lookup"><span data-stu-id="fbe5e-121">Redis Connection String.</span></span>
<span data-ttu-id="fbe5e-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbe5e-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="fbe5e-123">-Context</span></span>
<span data-ttu-id="fbe5e-124">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="fbe5e-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-125">This parameter is required.</span></span>

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

### <span data-ttu-id="fbe5e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbe5e-126">-DefaultProfile</span></span>
<span data-ttu-id="fbe5e-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbe5e-128">— Opis</span><span class="sxs-lookup"><span data-stu-id="fbe5e-128">-Description</span></span>
<span data-ttu-id="fbe5e-129">Opis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-129">Cache Description.</span></span>
<span data-ttu-id="fbe5e-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="fbe5e-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fbe5e-131">-InputObject</span></span>
<span data-ttu-id="fbe5e-132">Wystąpienie usługi PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="fbe5e-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbe5e-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fbe5e-134">-PassThru</span></span>
<span data-ttu-id="fbe5e-135">Jeśli zostanie określone, wówczas wystąpienie właściwości Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache, która reprezentuje zmodyfikowaną pamięć podręczną, zostanie zapisane w wyniku.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="fbe5e-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fbe5e-136">-ResourceId</span></span>
<span data-ttu-id="fbe5e-137">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="fbe5e-138">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-138">This parameter is required.</span></span>

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

### <span data-ttu-id="fbe5e-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fbe5e-139">-Confirm</span></span>
<span data-ttu-id="fbe5e-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbe5e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbe5e-141">-WhatIf</span></span>
<span data-ttu-id="fbe5e-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbe5e-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbe5e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbe5e-144">CommonParameters</span></span>
<span data-ttu-id="fbe5e-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbe5e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbe5e-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbe5e-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbe5e-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbe5e-147">INPUTS</span></span>

### <span data-ttu-id="fbe5e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="fbe5e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="fbe5e-149">System.String</span><span class="sxs-lookup"><span data-stu-id="fbe5e-149">System.String</span></span>

### <span data-ttu-id="fbe5e-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fbe5e-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="fbe5e-151">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="fbe5e-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fbe5e-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbe5e-152">OUTPUTS</span></span>

### <span data-ttu-id="fbe5e-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fbe5e-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="fbe5e-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbe5e-154">NOTES</span></span>

## <span data-ttu-id="fbe5e-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbe5e-155">RELATED LINKS</span></span>

[<span data-ttu-id="fbe5e-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fbe5e-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="fbe5e-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fbe5e-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="fbe5e-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="fbe5e-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
