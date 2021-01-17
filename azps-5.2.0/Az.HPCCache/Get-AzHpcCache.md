---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328244"
---
# <span data-ttu-id="e7e45-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e7e45-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="e7e45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7e45-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e45-103">Pobiera pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="e7e45-103">Gets a cache(s).</span></span>

## <span data-ttu-id="e7e45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7e45-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e7e45-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e7e45-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e45-106">Polecenie cmdlet **Get-AzHpcCache** pobiera jedną pamięć podręczną, pamięć podręczną w określonej grupie zasobów lub dużą listę pamięci podręcznych w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e7e45-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="e7e45-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7e45-107">EXAMPLES</span></span>

### <span data-ttu-id="e7e45-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e7e45-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="e7e45-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e7e45-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="e7e45-110">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e7e45-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="e7e45-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7e45-111">PARAMETERS</span></span>

### <span data-ttu-id="e7e45-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e45-112">-DefaultProfile</span></span>
<span data-ttu-id="e7e45-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7e45-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7e45-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7e45-114">-Name</span></span>
<span data-ttu-id="e7e45-115">Nazwa konkretnej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="e7e45-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="e7e45-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e45-116">-ResourceGroupName</span></span>
<span data-ttu-id="e7e45-117">Nazwa grupy zasobów, pod którą chcesz wyświetlić pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="e7e45-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="e7e45-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e45-118">CommonParameters</span></span>
<span data-ttu-id="e7e45-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7e45-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e45-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7e45-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e45-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7e45-121">INPUTS</span></span>

### <span data-ttu-id="e7e45-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e7e45-122">System.String</span></span>

## <span data-ttu-id="e7e45-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7e45-123">OUTPUTS</span></span>

### <span data-ttu-id="e7e45-124">Microsoft. Azure. PowerShell. polecenia. HPCCache. models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="e7e45-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="e7e45-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7e45-125">NOTES</span></span>

## <span data-ttu-id="e7e45-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7e45-126">RELATED LINKS</span></span>
