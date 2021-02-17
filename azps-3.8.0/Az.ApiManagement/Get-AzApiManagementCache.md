---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: fee978a1500c0fc472ec8015a3e8dbbbdc8015bd
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100407764"
---
# <span data-ttu-id="106e6-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="106e6-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="106e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="106e6-102">SYNOPSIS</span></span>
<span data-ttu-id="106e6-103">Uzyskaj szczegółowe informacje dotyczące pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="106e6-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="106e6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="106e6-104">SYNTAX</span></span>

### <span data-ttu-id="106e6-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="106e6-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="106e6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="106e6-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="106e6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="106e6-107">DESCRIPTION</span></span>
<span data-ttu-id="106e6-108">Uzyskaj szczegółowe informacje dotyczące pamięci podręcznej skonfigurowanej w usłudze zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="106e6-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="106e6-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="106e6-109">EXAMPLES</span></span>

### <span data-ttu-id="106e6-110">Przykład 1. Pobierz wszystkie pamięci podręczne</span><span class="sxs-lookup"><span data-stu-id="106e6-110">Example 1: Get all Caches</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-West-US
ServiceName       : contoso
```

<span data-ttu-id="106e6-111">Pobiera listę wszystkich pamięci podręcznych skonfigurowanych w usłudze zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="106e6-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="106e6-112">Przykład 2. Uzyskiwanie pamięci podręcznej określonej przez identyfikator westus</span><span class="sxs-lookup"><span data-stu-id="106e6-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCache -Context $apimContext -cacheId westus
```

```
CacheId           : westus
Description       : apim.redis.cache.windows.net
ConnectionString  : {{5cc1848125a3f724dcf9a928}}
ResourceId        : https://management.azure.com/subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-West-US/providers/Microsoft.Cache/Redis/apim
Id                : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/caches/westus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="106e6-113">Uzyskiwanie szczegółów określonej pamięci podręcznej skonfigurowanej dla zachód</span><span class="sxs-lookup"><span data-stu-id="106e6-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="106e6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="106e6-114">PARAMETERS</span></span>

### <span data-ttu-id="106e6-115">- CacheId</span><span class="sxs-lookup"><span data-stu-id="106e6-115">-CacheId</span></span>
<span data-ttu-id="106e6-116">Identyfikator pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="106e6-116">Identifier of a cache.</span></span>
<span data-ttu-id="106e6-117">Jeśli zostanie określona, spróbuje znaleźć pamięć podręczną według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="106e6-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="106e6-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="106e6-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="106e6-119">— kontekst</span><span class="sxs-lookup"><span data-stu-id="106e6-119">-Context</span></span>
<span data-ttu-id="106e6-120">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="106e6-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="106e6-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="106e6-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="106e6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="106e6-122">-DefaultProfile</span></span>
<span data-ttu-id="106e6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="106e6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="106e6-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="106e6-124">-ResourceId</span></span>
<span data-ttu-id="106e6-125">Identyfikator zasobu arm pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="106e6-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="106e6-126">Jeśli zostanie określona, spróbuje znaleźć pamięć podręczną według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="106e6-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="106e6-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="106e6-127">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="106e6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="106e6-128">CommonParameters</span></span>
<span data-ttu-id="106e6-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="106e6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="106e6-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="106e6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="106e6-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="106e6-131">INPUTS</span></span>

### <span data-ttu-id="106e6-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="106e6-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="106e6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="106e6-133">System.String</span></span>

## <span data-ttu-id="106e6-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="106e6-134">OUTPUTS</span></span>

### <span data-ttu-id="106e6-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="106e6-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="106e6-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="106e6-136">NOTES</span></span>

## <span data-ttu-id="106e6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="106e6-137">RELATED LINKS</span></span>

[<span data-ttu-id="106e6-138">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="106e6-138">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="106e6-139">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="106e6-139">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="106e6-140">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="106e6-140">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
