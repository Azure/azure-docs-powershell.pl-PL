---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200610"
---
# <span data-ttu-id="bedb0-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="bedb0-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="bedb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bedb0-102">SYNOPSIS</span></span>
<span data-ttu-id="bedb0-103">Tworzy nowy obiekt ADB Sql UniqueKey.</span><span class="sxs-lookup"><span data-stu-id="bedb0-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="bedb0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bedb0-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bedb0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bedb0-105">DESCRIPTION</span></span>
<span data-ttu-id="bedb0-106">Polecenie cmdlet **New-AzCosmosDBSqlUniqueKey** tworzy nowy obiekt typu PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="bedb0-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="bedb0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bedb0-107">EXAMPLES</span></span>

### <span data-ttu-id="bedb0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bedb0-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="bedb0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bedb0-109">PARAMETERS</span></span>

### <span data-ttu-id="bedb0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedb0-110">-DefaultProfile</span></span>
<span data-ttu-id="bedb0-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bedb0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bedb0-112">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="bedb0-112">-Path</span></span>
<span data-ttu-id="bedb0-113">Tablica ciągów wartości ścieżek</span><span class="sxs-lookup"><span data-stu-id="bedb0-113">Array of string of path values</span></span>

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

### <span data-ttu-id="bedb0-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedb0-114">CommonParameters</span></span>
<span data-ttu-id="bedb0-115">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bedb0-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedb0-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bedb0-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedb0-117">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bedb0-117">INPUTS</span></span>

### <span data-ttu-id="bedb0-118">Brak</span><span class="sxs-lookup"><span data-stu-id="bedb0-118">None</span></span>

## <span data-ttu-id="bedb0-119">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bedb0-119">OUTPUTS</span></span>

### <span data-ttu-id="bedb0-120">Microsoft.Azure.Commands.Dosdb.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="bedb0-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="bedb0-121">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bedb0-121">NOTES</span></span>

## <span data-ttu-id="bedb0-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bedb0-122">RELATED LINKS</span></span>
