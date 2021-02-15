---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398924"
---
# <span data-ttu-id="20e97-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20e97-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="20e97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20e97-102">SYNOPSIS</span></span>
<span data-ttu-id="20e97-103">aktualizuje pamięć podręczną w usłudze zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="20e97-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="20e97-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="20e97-104">SYNTAX</span></span>

### <span data-ttu-id="20e97-105">ExpandedParameters (domyślne)</span><span class="sxs-lookup"><span data-stu-id="20e97-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e97-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="20e97-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e97-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="20e97-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20e97-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="20e97-108">DESCRIPTION</span></span>
<span data-ttu-id="20e97-109">Polecenie cmdlet **Update-AzApiManagementCache** aktualizuje pamięć podręczną w usłudze ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="20e97-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="20e97-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="20e97-110">EXAMPLES</span></span>

### <span data-ttu-id="20e97-111">Przykład 1. Aktualizacja opisu pamięci podręcznej w centralu</span><span class="sxs-lookup"><span data-stu-id="20e97-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="20e97-112">Aktualizuje opis pamięci podręcznej w Środkowych Usach.</span><span class="sxs-lookup"><span data-stu-id="20e97-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="20e97-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20e97-113">PARAMETERS</span></span>

### <span data-ttu-id="20e97-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="20e97-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="20e97-115">Arm ResourceId wystąpienia usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="20e97-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="20e97-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="20e97-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="20e97-117">- CacheId</span><span class="sxs-lookup"><span data-stu-id="20e97-117">-CacheId</span></span>
<span data-ttu-id="20e97-118">Identyfikator nowej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="20e97-118">Identifier of new cache.</span></span>
<span data-ttu-id="20e97-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="20e97-119">This parameter is required.</span></span>

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

### <span data-ttu-id="20e97-120">- ConnectionString</span><span class="sxs-lookup"><span data-stu-id="20e97-120">-ConnectionString</span></span>
<span data-ttu-id="20e97-121">Redis Connection String (Redis Connection String).</span><span class="sxs-lookup"><span data-stu-id="20e97-121">Redis Connection String.</span></span>
<span data-ttu-id="20e97-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="20e97-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="20e97-123">— kontekst</span><span class="sxs-lookup"><span data-stu-id="20e97-123">-Context</span></span>
<span data-ttu-id="20e97-124">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="20e97-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="20e97-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="20e97-125">This parameter is required.</span></span>

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

### <span data-ttu-id="20e97-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e97-126">-DefaultProfile</span></span>
<span data-ttu-id="20e97-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="20e97-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20e97-128">— Opis</span><span class="sxs-lookup"><span data-stu-id="20e97-128">-Description</span></span>
<span data-ttu-id="20e97-129">Opis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="20e97-129">Cache Description.</span></span>
<span data-ttu-id="20e97-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="20e97-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="20e97-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20e97-131">-InputObject</span></span>
<span data-ttu-id="20e97-132">Wystąpienie usługi PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="20e97-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="20e97-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="20e97-133">This parameter is required.</span></span>

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

### <span data-ttu-id="20e97-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20e97-134">-PassThru</span></span>
<span data-ttu-id="20e97-135">Jeśli zostanie określone, wówczas wystąpienie właściwości Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache typ reprezentujący zmodyfikowaną pamięć podręczną zostanie zapisany w wyniku.</span><span class="sxs-lookup"><span data-stu-id="20e97-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="20e97-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20e97-136">-ResourceId</span></span>
<span data-ttu-id="20e97-137">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="20e97-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="20e97-138">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="20e97-138">This parameter is required.</span></span>

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

### <span data-ttu-id="20e97-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20e97-139">-Confirm</span></span>
<span data-ttu-id="20e97-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="20e97-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20e97-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20e97-141">-WhatIf</span></span>
<span data-ttu-id="20e97-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20e97-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20e97-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="20e97-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20e97-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e97-144">CommonParameters</span></span>
<span data-ttu-id="20e97-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e97-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e97-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20e97-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e97-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20e97-147">INPUTS</span></span>

### <span data-ttu-id="20e97-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="20e97-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20e97-149">System.String</span><span class="sxs-lookup"><span data-stu-id="20e97-149">System.String</span></span>

### <span data-ttu-id="20e97-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20e97-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="20e97-151">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="20e97-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="20e97-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="20e97-152">OUTPUTS</span></span>

### <span data-ttu-id="20e97-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20e97-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="20e97-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="20e97-154">NOTES</span></span>

## <span data-ttu-id="20e97-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20e97-155">RELATED LINKS</span></span>

[<span data-ttu-id="20e97-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20e97-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="20e97-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20e97-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="20e97-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20e97-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
