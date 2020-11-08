---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052608"
---
# <span data-ttu-id="a5730-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a5730-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="a5730-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5730-102">SYNOPSIS</span></span>
<span data-ttu-id="a5730-103">Tworzy nowy obiekt typu PSSqlConflictResolutionPolicy.</span><span class="sxs-lookup"><span data-stu-id="a5730-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="a5730-104">Może on zostać przekazany jako wartość parametru w parametrze Set-AzCosmosDBSqlContainer.</span><span class="sxs-lookup"><span data-stu-id="a5730-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="a5730-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5730-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5730-106">Opis</span><span class="sxs-lookup"><span data-stu-id="a5730-106">DESCRIPTION</span></span>
<span data-ttu-id="a5730-107">Obiekt odpowiadający ConflictResolutionPolicy API funkcji SQL.</span><span class="sxs-lookup"><span data-stu-id="a5730-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="a5730-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5730-108">EXAMPLES</span></span>

### <span data-ttu-id="a5730-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5730-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="a5730-110">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="a5730-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="a5730-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5730-111">PARAMETERS</span></span>

### <span data-ttu-id="a5730-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="a5730-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="a5730-113">Ma być dostarczany po wybraniu typu niestandardowy.</span><span class="sxs-lookup"><span data-stu-id="a5730-113">To be provided when the type is custom.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5730-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5730-114">-DefaultProfile</span></span>
<span data-ttu-id="a5730-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5730-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5730-116">-Path</span><span class="sxs-lookup"><span data-stu-id="a5730-116">-Path</span></span>
<span data-ttu-id="a5730-117">Ma być dostarczany, gdy typem jest LastWriterWins.</span><span class="sxs-lookup"><span data-stu-id="a5730-117">To be provided when the type is LastWriterWins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5730-118">-Type</span><span class="sxs-lookup"><span data-stu-id="a5730-118">-Type</span></span>
<span data-ttu-id="a5730-119">Może mieć wartości: LastWriterWins, Custom, Manual.</span><span class="sxs-lookup"><span data-stu-id="a5730-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5730-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5730-120">CommonParameters</span></span>
<span data-ttu-id="a5730-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5730-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5730-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a5730-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5730-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5730-123">INPUTS</span></span>

### <span data-ttu-id="a5730-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a5730-124">None</span></span>

## <span data-ttu-id="a5730-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5730-125">OUTPUTS</span></span>

### <span data-ttu-id="a5730-126">Microsoft. Azure. Commands. CosmosDB. models. PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="a5730-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="a5730-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5730-127">NOTES</span></span>

## <span data-ttu-id="a5730-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5730-128">RELATED LINKS</span></span>
