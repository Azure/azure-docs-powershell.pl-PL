---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: FA99C137-68E3-47D3-A0AC-FE33A481BE66
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscachediagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCacheDiagnostic.md
ms.openlocfilehash: 60c552b0878907c7b2c4a56d8068968c3ace862a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186554"
---
# <span data-ttu-id="dde3f-101">Set-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dde3f-101">Set-AzRedisCacheDiagnostic</span></span>

## <span data-ttu-id="dde3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dde3f-102">SYNOPSIS</span></span>
<span data-ttu-id="dde3f-103">Włącza diagnostykę w usłudze Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="dde3f-103">Enables diagnostics on an Azure Redis Cache.</span></span>

## <span data-ttu-id="dde3f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dde3f-104">SYNTAX</span></span>

```
Set-AzRedisCacheDiagnostic [-ResourceGroupName <String>] -Name <String> -StorageAccountId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dde3f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dde3f-105">DESCRIPTION</span></span>
<span data-ttu-id="dde3f-106">Polecenie **cmdlet Set-AzRedisCacheDiagnostic** umożliwia diagnostykę dla pamięci podręcznej Azure Redis Cache.</span><span class="sxs-lookup"><span data-stu-id="dde3f-106">The **Set-AzRedisCacheDiagnostic** cmdlet enables diagnostics for an Azure Redis Cache.</span></span>

## <span data-ttu-id="dde3f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dde3f-107">EXAMPLES</span></span>

### <span data-ttu-id="dde3f-108">Przykład 1. Włączanie diagnostyki</span><span class="sxs-lookup"><span data-stu-id="dde3f-108">Example 1: Enable diagnostics</span></span>
```
PS C:\>Set-AzRedisCacheDiagnostic -ResourceGroupName "ContosoResourceGroup" -Name "PeakCache" -StorageAccountId "/subscriptions/fffff139-aaaa-bbbb-cccc-21f21f35806e/resourcegroups/myresourcegroup/providers/Microsoft.Storage/storageAccounts/mystorageaccount"
```

<span data-ttu-id="dde3f-109">To polecenie umożliwia diagnostykę dla pamięci podręcznej Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="dde3f-109">This command enables diagnostics for an Azure Redis cache.</span></span>
<span data-ttu-id="dde3f-110">To polecenie włączy diagnostykę lub zaktualizuje konto magazynu dla wszystkich funkcji Azure Redis Cache w tym samym regionie subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="dde3f-110">This command will enable diagnostics or update the storage account for all Azure Redis Caches in the same region for the subscription.</span></span>

## <span data-ttu-id="dde3f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dde3f-111">PARAMETERS</span></span>

### <span data-ttu-id="dde3f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde3f-112">-DefaultProfile</span></span>
<span data-ttu-id="dde3f-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dde3f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde3f-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dde3f-114">-Name</span></span>
<span data-ttu-id="dde3f-115">Określa nazwę pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="dde3f-115">Specifies the name of the cache.</span></span>

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

### <span data-ttu-id="dde3f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde3f-116">-ResourceGroupName</span></span>
<span data-ttu-id="dde3f-117">Określa nazwę grupy zasobów, która zawiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="dde3f-117">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="dde3f-118">- StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="dde3f-118">-StorageAccountId</span></span>
<span data-ttu-id="dde3f-119">Określa identyfikator zasobu konta magazynu używanego do przechowywania danych diagnostycznych.</span><span class="sxs-lookup"><span data-stu-id="dde3f-119">Specifies the resource ID of the storage account used to store the diagnostics data.</span></span>

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

### <span data-ttu-id="dde3f-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dde3f-120">-Confirm</span></span>
<span data-ttu-id="dde3f-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dde3f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dde3f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde3f-122">-WhatIf</span></span>
<span data-ttu-id="dde3f-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde3f-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dde3f-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dde3f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dde3f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde3f-125">CommonParameters</span></span>
<span data-ttu-id="dde3f-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde3f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde3f-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dde3f-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde3f-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dde3f-128">INPUTS</span></span>

### <span data-ttu-id="dde3f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="dde3f-129">System.String</span></span>

## <span data-ttu-id="dde3f-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dde3f-130">OUTPUTS</span></span>

### <span data-ttu-id="dde3f-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="dde3f-131">System.Void</span></span>

## <span data-ttu-id="dde3f-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dde3f-132">NOTES</span></span>
* <span data-ttu-id="dde3f-133">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span><span class="sxs-lookup"><span data-stu-id="dde3f-133">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="dde3f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dde3f-134">RELATED LINKS</span></span>

[<span data-ttu-id="dde3f-135">Remove-AzRedisCacheDiagnostic</span><span class="sxs-lookup"><span data-stu-id="dde3f-135">Remove-AzRedisCacheDiagnostic</span></span>](./Remove-AzRedisCacheDiagnostic.md)


