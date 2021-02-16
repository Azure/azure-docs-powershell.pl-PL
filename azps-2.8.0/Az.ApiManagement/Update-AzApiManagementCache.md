---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: c8c535168a86607daab27ab89340d231bb4e4bd3
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406897"
---
# <span data-ttu-id="e03d8-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e03d8-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="e03d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e03d8-102">SYNOPSIS</span></span>
<span data-ttu-id="e03d8-103">aktualizuje pamięć podręczną w usłudze zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="e03d8-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="e03d8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e03d8-104">SYNTAX</span></span>

### <span data-ttu-id="e03d8-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e03d8-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e03d8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e03d8-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e03d8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e03d8-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e03d8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e03d8-108">DESCRIPTION</span></span>
<span data-ttu-id="e03d8-109">Polecenie cmdlet **Update-AzApiManagementCache** aktualizuje pamięć podręczną w usłudze ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e03d8-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="e03d8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e03d8-110">EXAMPLES</span></span>

### <span data-ttu-id="e03d8-111">Przykład 1. Aktualizacja opisu pamięci podręcznej w centralu</span><span class="sxs-lookup"><span data-stu-id="e03d8-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="e03d8-112">Aktualizuje opis pamięci podręcznej w Środkowych Usach.</span><span class="sxs-lookup"><span data-stu-id="e03d8-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="e03d8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e03d8-113">PARAMETERS</span></span>

### <span data-ttu-id="e03d8-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="e03d8-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="e03d8-115">Arm ResourceId wystąpienia usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="e03d8-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="e03d8-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e03d8-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="e03d8-117">- CacheId</span><span class="sxs-lookup"><span data-stu-id="e03d8-117">-CacheId</span></span>
<span data-ttu-id="e03d8-118">Identyfikator nowej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="e03d8-118">Identifier of new cache.</span></span>
<span data-ttu-id="e03d8-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e03d8-119">This parameter is required.</span></span>

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

### <span data-ttu-id="e03d8-120">- ConnectionString</span><span class="sxs-lookup"><span data-stu-id="e03d8-120">-ConnectionString</span></span>
<span data-ttu-id="e03d8-121">Redis Connection String (Redis Connection String).</span><span class="sxs-lookup"><span data-stu-id="e03d8-121">Redis Connection String.</span></span>
<span data-ttu-id="e03d8-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e03d8-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="e03d8-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e03d8-123">-Context</span></span>
<span data-ttu-id="e03d8-124">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e03d8-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e03d8-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e03d8-125">This parameter is required.</span></span>

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

### <span data-ttu-id="e03d8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e03d8-126">-DefaultProfile</span></span>
<span data-ttu-id="e03d8-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e03d8-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e03d8-128">— Opis</span><span class="sxs-lookup"><span data-stu-id="e03d8-128">-Description</span></span>
<span data-ttu-id="e03d8-129">Opis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="e03d8-129">Cache Description.</span></span>
<span data-ttu-id="e03d8-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e03d8-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="e03d8-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e03d8-131">-InputObject</span></span>
<span data-ttu-id="e03d8-132">Wystąpienie usługi PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="e03d8-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="e03d8-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e03d8-133">This parameter is required.</span></span>

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

### <span data-ttu-id="e03d8-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e03d8-134">-PassThru</span></span>
<span data-ttu-id="e03d8-135">Jeśli zostanie określone, wówczas wystąpienie właściwości Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache, która reprezentuje zmodyfikowaną pamięć podręczną, zostanie zapisane w wyniku.</span><span class="sxs-lookup"><span data-stu-id="e03d8-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="e03d8-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e03d8-136">-ResourceId</span></span>
<span data-ttu-id="e03d8-137">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="e03d8-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="e03d8-138">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e03d8-138">This parameter is required.</span></span>

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

### <span data-ttu-id="e03d8-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e03d8-139">-Confirm</span></span>
<span data-ttu-id="e03d8-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e03d8-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e03d8-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e03d8-141">-WhatIf</span></span>
<span data-ttu-id="e03d8-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e03d8-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e03d8-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e03d8-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e03d8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e03d8-144">CommonParameters</span></span>
<span data-ttu-id="e03d8-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e03d8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e03d8-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e03d8-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e03d8-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e03d8-147">INPUTS</span></span>

### <span data-ttu-id="e03d8-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e03d8-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e03d8-149">System.String</span><span class="sxs-lookup"><span data-stu-id="e03d8-149">System.String</span></span>

### <span data-ttu-id="e03d8-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e03d8-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="e03d8-151">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e03d8-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e03d8-152">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e03d8-152">OUTPUTS</span></span>

### <span data-ttu-id="e03d8-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e03d8-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="e03d8-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e03d8-154">NOTES</span></span>

## <span data-ttu-id="e03d8-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e03d8-155">RELATED LINKS</span></span>

[<span data-ttu-id="e03d8-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e03d8-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="e03d8-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e03d8-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="e03d8-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="e03d8-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
