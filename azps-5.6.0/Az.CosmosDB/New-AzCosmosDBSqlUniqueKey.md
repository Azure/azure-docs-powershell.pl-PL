---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: b172c5e22c26cba8d88d188198868da720d611d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990326"
---
# <span data-ttu-id="d142a-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="d142a-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="d142a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d142a-102">SYNOPSIS</span></span>
<span data-ttu-id="d142a-103">Tworzy nowy obiekt Adb Sql UniqueKey.</span><span class="sxs-lookup"><span data-stu-id="d142a-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="d142a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d142a-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d142a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d142a-105">DESCRIPTION</span></span>
<span data-ttu-id="d142a-106">Polecenie cmdlet **New-AzCosmosDBSqlUniqueKey** tworzy nowy obiekt typu PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="d142a-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="d142a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d142a-107">EXAMPLES</span></span>

### <span data-ttu-id="d142a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d142a-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="d142a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d142a-109">PARAMETERS</span></span>

### <span data-ttu-id="d142a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d142a-110">-DefaultProfile</span></span>
<span data-ttu-id="d142a-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d142a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d142a-112">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="d142a-112">-Path</span></span>
<span data-ttu-id="d142a-113">Tablica ciągów wartości ścieżek</span><span class="sxs-lookup"><span data-stu-id="d142a-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d142a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d142a-114">CommonParameters</span></span>
<span data-ttu-id="d142a-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d142a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d142a-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d142a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d142a-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d142a-117">INPUTS</span></span>

### <span data-ttu-id="d142a-118">Brak</span><span class="sxs-lookup"><span data-stu-id="d142a-118">None</span></span>

## <span data-ttu-id="d142a-119">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d142a-119">OUTPUTS</span></span>

### <span data-ttu-id="d142a-120">Microsoft.Azure.Commands.Dosdb.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="d142a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="d142a-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d142a-121">NOTES</span></span>

## <span data-ttu-id="d142a-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d142a-122">RELATED LINKS</span></span>
