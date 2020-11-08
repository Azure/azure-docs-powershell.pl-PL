---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCache.md
ms.openlocfilehash: 757332267d2db2f797bb2f7ca2a39dbb32ee06c7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050908"
---
# <span data-ttu-id="20282-101">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20282-101">Get-AzApiManagementCache</span></span>

## <span data-ttu-id="20282-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20282-102">SYNOPSIS</span></span>
<span data-ttu-id="20282-103">Zapoznaj się z informacjami na temat pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="20282-103">Get the details of the Cache.</span></span>

## <span data-ttu-id="20282-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20282-104">SYNTAX</span></span>

### <span data-ttu-id="20282-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="20282-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20282-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20282-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCache -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20282-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20282-107">DESCRIPTION</span></span>
<span data-ttu-id="20282-108">Uzyskaj szczegółowe informacje o pamięci podręcznej skonfigurowanej w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="20282-108">Get the details of the Cache configured in Api Management service.</span></span>

## <span data-ttu-id="20282-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20282-109">EXAMPLES</span></span>

### <span data-ttu-id="20282-110">Przykład 1: pobieranie wszystkich pamięci podręcznych</span><span class="sxs-lookup"><span data-stu-id="20282-110">Example 1: Get all Caches</span></span>
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

<span data-ttu-id="20282-111">Pobiera listę wszystkich buforów skonfigurowanych w usłudze zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="20282-111">Gets a list of all the Caches configured in the Api Management service.</span></span>

### <span data-ttu-id="20282-112">Przykład 2: uzyskiwanie pamięci podręcznej określonej przez identyfikator zachód</span><span class="sxs-lookup"><span data-stu-id="20282-112">Example 2: Get the Cache specified by the Identifier westus</span></span>
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

<span data-ttu-id="20282-113">Uzyskiwanie szczegółowych informacji o określonej pamięci podręcznej skonfigurowanej dla zachodniego</span><span class="sxs-lookup"><span data-stu-id="20282-113">Get the details of the specified Cache configured for westus</span></span>

## <span data-ttu-id="20282-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20282-114">PARAMETERS</span></span>

### <span data-ttu-id="20282-115">-CacheId</span><span class="sxs-lookup"><span data-stu-id="20282-115">-CacheId</span></span>
<span data-ttu-id="20282-116">Identyfikator pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="20282-116">Identifier of a cache.</span></span>
<span data-ttu-id="20282-117">Jeśli zostanie określona, spróbuje znaleźć pamięć podręczną przy użyciu identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="20282-117">If specified will try to find cache by the identifier.</span></span>
<span data-ttu-id="20282-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="20282-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="20282-119">-Context</span><span class="sxs-lookup"><span data-stu-id="20282-119">-Context</span></span>
<span data-ttu-id="20282-120">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="20282-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="20282-121">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="20282-121">This parameter is required.</span></span>

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

### <span data-ttu-id="20282-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20282-122">-DefaultProfile</span></span>
<span data-ttu-id="20282-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20282-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20282-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20282-124">-ResourceId</span></span>
<span data-ttu-id="20282-125">Identyfikator zasobu ARM pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="20282-125">Arm Resource Identifier of a cache.</span></span> <span data-ttu-id="20282-126">Jeśli zostanie określona, spróbuje znaleźć pamięć podręczną przy użyciu identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="20282-126">If specified will try to find cache by the identifier.</span></span> <span data-ttu-id="20282-127">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="20282-127">This parameter is required.</span></span>

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

### <span data-ttu-id="20282-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20282-128">CommonParameters</span></span>
<span data-ttu-id="20282-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20282-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20282-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20282-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20282-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20282-131">INPUTS</span></span>

### <span data-ttu-id="20282-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="20282-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="20282-133">System. String</span><span class="sxs-lookup"><span data-stu-id="20282-133">System.String</span></span>

## <span data-ttu-id="20282-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20282-134">OUTPUTS</span></span>

### <span data-ttu-id="20282-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20282-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="20282-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20282-136">NOTES</span></span>

## <span data-ttu-id="20282-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20282-137">RELATED LINKS</span></span>

[<span data-ttu-id="20282-138">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20282-138">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache)

[<span data-ttu-id="20282-139">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20282-139">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="20282-140">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="20282-140">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)