---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195410"
---
# <span data-ttu-id="da233-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="da233-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="da233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da233-102">SYNOPSIS</span></span>
<span data-ttu-id="da233-103">Tworzy nową jednostkę pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="da233-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="da233-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da233-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da233-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="da233-105">DESCRIPTION</span></span>
<span data-ttu-id="da233-106">Polecenie cmdlet **New-AzApiManagementCache** tworzy nową jednostkę pamięci podręcznej w usłudze zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="da233-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="da233-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da233-107">EXAMPLES</span></span>

### <span data-ttu-id="da233-108">Przykład 1. Tworzenie nowej jednostki pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="da233-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="da233-109">Polecenia cmdlet tworzą nową jednostkę pamięci podręcznej w głównej lokalizacji usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="da233-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="da233-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da233-110">PARAMETERS</span></span>

### <span data-ttu-id="da233-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="da233-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="da233-112">Arm ResourceId wystąpienia usługi Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="da233-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="da233-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="da233-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="da233-114">- CacheId</span><span class="sxs-lookup"><span data-stu-id="da233-114">-CacheId</span></span>
<span data-ttu-id="da233-115">Identyfikator nowej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="da233-115">Identifier of new cache.</span></span>
<span data-ttu-id="da233-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="da233-116">This parameter is optional.</span></span>
<span data-ttu-id="da233-117">Jeśli nie określono, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="da233-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="da233-118">- ConnectionString</span><span class="sxs-lookup"><span data-stu-id="da233-118">-ConnectionString</span></span>
<span data-ttu-id="da233-119">Redis Connection String (Redis Connection String).</span><span class="sxs-lookup"><span data-stu-id="da233-119">Redis Connection String.</span></span>
<span data-ttu-id="da233-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="da233-120">This parameter is required.</span></span>

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

### <span data-ttu-id="da233-121">— kontekst</span><span class="sxs-lookup"><span data-stu-id="da233-121">-Context</span></span>
<span data-ttu-id="da233-122">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="da233-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="da233-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="da233-123">This parameter is required.</span></span>

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

### <span data-ttu-id="da233-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da233-124">-DefaultProfile</span></span>
<span data-ttu-id="da233-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="da233-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da233-126">— Opis</span><span class="sxs-lookup"><span data-stu-id="da233-126">-Description</span></span>
<span data-ttu-id="da233-127">Opis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="da233-127">Cache Description.</span></span>
<span data-ttu-id="da233-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="da233-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="da233-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da233-129">-Confirm</span></span>
<span data-ttu-id="da233-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="da233-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da233-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da233-131">-WhatIf</span></span>
<span data-ttu-id="da233-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da233-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da233-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="da233-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da233-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da233-134">CommonParameters</span></span>
<span data-ttu-id="da233-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da233-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da233-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da233-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da233-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da233-137">INPUTS</span></span>

### <span data-ttu-id="da233-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="da233-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="da233-139">System.String</span><span class="sxs-lookup"><span data-stu-id="da233-139">System.String</span></span>

## <span data-ttu-id="da233-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da233-140">OUTPUTS</span></span>

### <span data-ttu-id="da233-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="da233-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="da233-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da233-142">NOTES</span></span>

## <span data-ttu-id="da233-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da233-143">RELATED LINKS</span></span>

[<span data-ttu-id="da233-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="da233-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="da233-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="da233-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="da233-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="da233-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
