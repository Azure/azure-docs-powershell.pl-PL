---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234210"
---
# <span data-ttu-id="a619b-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a619b-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="a619b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a619b-102">SYNOPSIS</span></span>
<span data-ttu-id="a619b-103">Tworzy nową jednostkę pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="a619b-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="a619b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a619b-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a619b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a619b-105">DESCRIPTION</span></span>
<span data-ttu-id="a619b-106">Polecenie cmdlet **New-AzApiManagementCache** tworzy nową jednostkę pamięci podręcznej w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="a619b-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="a619b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a619b-107">EXAMPLES</span></span>

### <span data-ttu-id="a619b-108">Przykład 1. Tworzenie nowej jednostki pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="a619b-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="a619b-109">Polecenia cmdlet tworzą nową jednostkę pamięci podręcznej w lokalizacji głównej usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="a619b-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="a619b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a619b-110">PARAMETERS</span></span>

### <span data-ttu-id="a619b-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="a619b-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="a619b-112">Identyfikator zasobu ARM w wystąpieniu pamięci podręcznej usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="a619b-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="a619b-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a619b-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="a619b-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="a619b-114">-CacheId</span></span>
<span data-ttu-id="a619b-115">Identyfikator nowej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a619b-115">Identifier of new cache.</span></span>
<span data-ttu-id="a619b-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a619b-116">This parameter is optional.</span></span>
<span data-ttu-id="a619b-117">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="a619b-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="a619b-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="a619b-118">-ConnectionString</span></span>
<span data-ttu-id="a619b-119">Parametry połączenia Redis.</span><span class="sxs-lookup"><span data-stu-id="a619b-119">Redis Connection String.</span></span>
<span data-ttu-id="a619b-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a619b-120">This parameter is required.</span></span>

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

### <span data-ttu-id="a619b-121">-Context</span><span class="sxs-lookup"><span data-stu-id="a619b-121">-Context</span></span>
<span data-ttu-id="a619b-122">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a619b-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a619b-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="a619b-123">This parameter is required.</span></span>

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

### <span data-ttu-id="a619b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a619b-124">-DefaultProfile</span></span>
<span data-ttu-id="a619b-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a619b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a619b-126">— Opis</span><span class="sxs-lookup"><span data-stu-id="a619b-126">-Description</span></span>
<span data-ttu-id="a619b-127">Opis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="a619b-127">Cache Description.</span></span>
<span data-ttu-id="a619b-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="a619b-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="a619b-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a619b-129">-Confirm</span></span>
<span data-ttu-id="a619b-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a619b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a619b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a619b-131">-WhatIf</span></span>
<span data-ttu-id="a619b-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a619b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a619b-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a619b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a619b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a619b-134">CommonParameters</span></span>
<span data-ttu-id="a619b-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a619b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a619b-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a619b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a619b-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a619b-137">INPUTS</span></span>

### <span data-ttu-id="a619b-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a619b-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a619b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a619b-139">System.String</span></span>

## <span data-ttu-id="a619b-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a619b-140">OUTPUTS</span></span>

### <span data-ttu-id="a619b-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a619b-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="a619b-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a619b-142">NOTES</span></span>

## <span data-ttu-id="a619b-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a619b-143">RELATED LINKS</span></span>

[<span data-ttu-id="a619b-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a619b-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="a619b-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a619b-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="a619b-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="a619b-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
