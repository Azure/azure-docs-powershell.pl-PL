---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307027"
---
# <span data-ttu-id="166ce-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="166ce-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="166ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="166ce-102">SYNOPSIS</span></span>
<span data-ttu-id="166ce-103">Tworzy nowy indeks MongoDB CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="166ce-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="166ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="166ce-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="166ce-105">Opis</span><span class="sxs-lookup"><span data-stu-id="166ce-105">DESCRIPTION</span></span>
<span data-ttu-id="166ce-106">**Nowy — AzCosmosDBMongoDBIndex** tworzy nowy CosmosDB indeks MongoDB.</span><span class="sxs-lookup"><span data-stu-id="166ce-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="166ce-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="166ce-107">EXAMPLES</span></span>

### <span data-ttu-id="166ce-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="166ce-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="166ce-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="166ce-109">PARAMETERS</span></span>

### <span data-ttu-id="166ce-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="166ce-110">-DefaultProfile</span></span>
<span data-ttu-id="166ce-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="166ce-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="166ce-112">-Key</span><span class="sxs-lookup"><span data-stu-id="166ce-112">-Key</span></span>
<span data-ttu-id="166ce-113">Tablica wartości klucza jako ciągi.</span><span class="sxs-lookup"><span data-stu-id="166ce-113">Array of key values as strings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166ce-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="166ce-114">-TtlInSeconds</span></span>
<span data-ttu-id="166ce-115">Liczba sekund, po upływie których indeks wygasa.</span><span class="sxs-lookup"><span data-stu-id="166ce-115">Number of seconds after which the index expires.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166ce-116">— Unikatowy</span><span class="sxs-lookup"><span data-stu-id="166ce-116">-Unique</span></span>
<span data-ttu-id="166ce-117">Wartość logiczna wskazująca, czy indeks jest unikatowy, czy nie.</span><span class="sxs-lookup"><span data-stu-id="166ce-117">Bool to indicate if the index is unique or not.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="166ce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="166ce-118">CommonParameters</span></span>
<span data-ttu-id="166ce-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="166ce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="166ce-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="166ce-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="166ce-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="166ce-121">INPUTS</span></span>

### <span data-ttu-id="166ce-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="166ce-122">None</span></span>

## <span data-ttu-id="166ce-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="166ce-123">OUTPUTS</span></span>

### <span data-ttu-id="166ce-124">Microsoft. Azure. Commands. CosmosDB. models. PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="166ce-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="166ce-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="166ce-125">NOTES</span></span>

## <span data-ttu-id="166ce-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="166ce-126">RELATED LINKS</span></span>
