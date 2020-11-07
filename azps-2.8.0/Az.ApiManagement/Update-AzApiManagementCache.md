---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: c912bc82f579bdd099ec63d2e09c4e762684329c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706881"
---
# <span data-ttu-id="a9f69-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a9f69-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="a9f69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9f69-102">SYNOPSIS</span></span>
<span data-ttu-id="a9f69-103">aktualizuje pamięć podręczną w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="a9f69-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="a9f69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9f69-104">SYNTAX</span></span>

### <span data-ttu-id="a9f69-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9f69-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9f69-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a9f69-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9f69-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9f69-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9f69-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9f69-108">DESCRIPTION</span></span>
<span data-ttu-id="a9f69-109">Aktualizacja polecenia cmdlet **-AzApiManagementCache** aktualizuje pamięć podręczną w usłudze ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="a9f69-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="a9f69-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9f69-110">EXAMPLES</span></span>

### <span data-ttu-id="a9f69-111">Przykład 1: aktualizuje Opis pamięci podręcznej w centrum centralnym</span><span class="sxs-lookup"><span data-stu-id="a9f69-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="a9f69-112">Aktualizuje Opis pamięci podręcznej w obszarze Centrala amerykańska.</span><span class="sxs-lookup"><span data-stu-id="a9f69-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="a9f69-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9f69-113">PARAMETERS</span></span>

### <span data-ttu-id="a9f69-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="a9f69-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="a9f69-115">Identyfikator zasobu ARM w wystąpieniu pamięci podręcznej usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a9f69-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="a9f69-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a9f69-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9f69-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="a9f69-117">-CacheId</span></span>
<span data-ttu-id="a9f69-118">Identyfikator nowej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a9f69-118">Identifier of new cache.</span></span>
<span data-ttu-id="a9f69-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a9f69-119">This parameter is required.</span></span>

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

### <span data-ttu-id="a9f69-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a9f69-120">-ConnectionString</span></span>
<span data-ttu-id="a9f69-121">Parametry połączenia Redis.</span><span class="sxs-lookup"><span data-stu-id="a9f69-121">Redis Connection String.</span></span>
<span data-ttu-id="a9f69-122">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a9f69-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9f69-123">-Context</span><span class="sxs-lookup"><span data-stu-id="a9f69-123">-Context</span></span>
<span data-ttu-id="a9f69-124">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a9f69-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a9f69-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a9f69-125">This parameter is required.</span></span>

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

### <span data-ttu-id="a9f69-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9f69-126">-DefaultProfile</span></span>
<span data-ttu-id="a9f69-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9f69-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9f69-128">— Opis</span><span class="sxs-lookup"><span data-stu-id="a9f69-128">-Description</span></span>
<span data-ttu-id="a9f69-129">Opis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a9f69-129">Cache Description.</span></span>
<span data-ttu-id="a9f69-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a9f69-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="a9f69-131">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9f69-131">-InputObject</span></span>
<span data-ttu-id="a9f69-132">Wystąpienie PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="a9f69-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="a9f69-133">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a9f69-133">This parameter is required.</span></span>

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

### <span data-ttu-id="a9f69-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9f69-134">-PassThru</span></span>
<span data-ttu-id="a9f69-135">Jeśli zostanie określone, wystąpienie systemu Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCache reprezentujące zmodyfikowaną pamięć podręczną zostanie zapisana w wyniku.</span><span class="sxs-lookup"><span data-stu-id="a9f69-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="a9f69-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9f69-136">-ResourceId</span></span>
<span data-ttu-id="a9f69-137">Identyfikator zasobu ARM w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a9f69-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="a9f69-138">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a9f69-138">This parameter is required.</span></span>

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

### <span data-ttu-id="a9f69-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9f69-139">-Confirm</span></span>
<span data-ttu-id="a9f69-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9f69-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9f69-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9f69-141">-WhatIf</span></span>
<span data-ttu-id="a9f69-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9f69-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9f69-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9f69-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9f69-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9f69-144">CommonParameters</span></span>
<span data-ttu-id="a9f69-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9f69-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9f69-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9f69-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9f69-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9f69-147">INPUTS</span></span>

### <span data-ttu-id="a9f69-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a9f69-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a9f69-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a9f69-149">System.String</span></span>

### <span data-ttu-id="a9f69-150">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a9f69-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="a9f69-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a9f69-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a9f69-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9f69-152">OUTPUTS</span></span>

### <span data-ttu-id="a9f69-153">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a9f69-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="a9f69-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9f69-154">NOTES</span></span>

## <span data-ttu-id="a9f69-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9f69-155">RELATED LINKS</span></span>

[<span data-ttu-id="a9f69-156">Nowe — AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a9f69-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache)

[<span data-ttu-id="a9f69-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a9f69-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="a9f69-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a9f69-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)