---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: 4ae5bdd5dc9c15ab72b2f35f5d67eeaa732296bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051212"
---
# <span data-ttu-id="8e641-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e641-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="8e641-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e641-102">SYNOPSIS</span></span>
<span data-ttu-id="8e641-103">Tworzy nową jednostkę pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="8e641-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="8e641-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e641-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e641-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8e641-105">DESCRIPTION</span></span>
<span data-ttu-id="8e641-106">Polecenie cmdlet **New-AzApiManagementCache** tworzy nową jednostkę pamięci podręcznej w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="8e641-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="8e641-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e641-107">EXAMPLES</span></span>

### <span data-ttu-id="8e641-108">Przykład 1. Tworzenie nowej jednostki pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="8e641-108">Example 1 : Create a new Cache entity</span></span>
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

<span data-ttu-id="8e641-109">Polecenia cmdlet tworzą nową jednostkę pamięci podręcznej w lokalizacji głównej usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="8e641-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="8e641-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e641-110">PARAMETERS</span></span>

### <span data-ttu-id="8e641-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="8e641-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="8e641-112">Identyfikator zasobu ARM w wystąpieniu pamięci podręcznej usługi Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="8e641-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="8e641-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8e641-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e641-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="8e641-114">-CacheId</span></span>
<span data-ttu-id="8e641-115">Identyfikator nowej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="8e641-115">Identifier of new cache.</span></span>
<span data-ttu-id="8e641-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8e641-116">This parameter is optional.</span></span>
<span data-ttu-id="8e641-117">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="8e641-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="8e641-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="8e641-118">-ConnectionString</span></span>
<span data-ttu-id="8e641-119">Parametry połączenia Redis.</span><span class="sxs-lookup"><span data-stu-id="8e641-119">Redis Connection String.</span></span>
<span data-ttu-id="8e641-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8e641-120">This parameter is required.</span></span>

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

### <span data-ttu-id="8e641-121">-Context</span><span class="sxs-lookup"><span data-stu-id="8e641-121">-Context</span></span>
<span data-ttu-id="8e641-122">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8e641-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8e641-123">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8e641-123">This parameter is required.</span></span>

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

### <span data-ttu-id="8e641-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e641-124">-DefaultProfile</span></span>
<span data-ttu-id="8e641-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e641-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e641-126">— Opis</span><span class="sxs-lookup"><span data-stu-id="8e641-126">-Description</span></span>
<span data-ttu-id="8e641-127">Opis pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="8e641-127">Cache Description.</span></span>
<span data-ttu-id="8e641-128">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8e641-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="8e641-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e641-129">-Confirm</span></span>
<span data-ttu-id="8e641-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e641-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e641-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e641-131">-WhatIf</span></span>
<span data-ttu-id="8e641-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e641-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e641-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e641-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e641-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e641-134">CommonParameters</span></span>
<span data-ttu-id="8e641-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e641-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e641-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e641-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e641-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e641-137">INPUTS</span></span>

### <span data-ttu-id="8e641-138">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8e641-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8e641-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8e641-139">System.String</span></span>

## <span data-ttu-id="8e641-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e641-140">OUTPUTS</span></span>

### <span data-ttu-id="8e641-141">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e641-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="8e641-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e641-142">NOTES</span></span>

## <span data-ttu-id="8e641-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e641-143">RELATED LINKS</span></span>

[<span data-ttu-id="8e641-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e641-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="8e641-145">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e641-145">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="8e641-146">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="8e641-146">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
