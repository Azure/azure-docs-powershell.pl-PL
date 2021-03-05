---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: c88e7d2b930eb7d04760f963a5ab8ea60ab8d455
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012097"
---
# <span data-ttu-id="29695-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="29695-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="29695-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29695-102">SYNOPSIS</span></span>
<span data-ttu-id="29695-103">Pobiera pamięci podręczne.</span><span class="sxs-lookup"><span data-stu-id="29695-103">Gets a cache(s).</span></span>

## <span data-ttu-id="29695-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="29695-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="29695-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="29695-105">DESCRIPTION</span></span>
<span data-ttu-id="29695-106">Polecenie **cmdlet Get-AzHpcCache** pobiera jedną pamięć podręczną, pamięci podręczne w określonej grupie zasobów lub listę pamięci podręcznych dla całej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="29695-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="29695-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="29695-107">EXAMPLES</span></span>

### <span data-ttu-id="29695-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="29695-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="29695-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="29695-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="29695-110">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="29695-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="29695-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29695-111">PARAMETERS</span></span>

### <span data-ttu-id="29695-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29695-112">-DefaultProfile</span></span>
<span data-ttu-id="29695-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="29695-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29695-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="29695-114">-Name</span></span>
<span data-ttu-id="29695-115">Nazwa określonej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="29695-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29695-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29695-116">-ResourceGroupName</span></span>
<span data-ttu-id="29695-117">Nazwa grupy zasobów, w ramach której mają zostać zapisane pamięci podręczne.</span><span class="sxs-lookup"><span data-stu-id="29695-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="29695-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29695-118">CommonParameters</span></span>
<span data-ttu-id="29695-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29695-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29695-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29695-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29695-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29695-121">INPUTS</span></span>

### <span data-ttu-id="29695-122">System.String</span><span class="sxs-lookup"><span data-stu-id="29695-122">System.String</span></span>

## <span data-ttu-id="29695-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29695-123">OUTPUTS</span></span>

### <span data-ttu-id="29695-124">Microsoft.Azure.PowerShell.Cmdlet.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="29695-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="29695-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="29695-125">NOTES</span></span>

## <span data-ttu-id="29695-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29695-126">RELATED LINKS</span></span>
