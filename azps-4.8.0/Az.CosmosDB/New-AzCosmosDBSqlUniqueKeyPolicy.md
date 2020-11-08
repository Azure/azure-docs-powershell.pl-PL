---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221831"
---
# <span data-ttu-id="a6d85-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a6d85-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="a6d85-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a6d85-102">SYNOPSIS</span></span>
<span data-ttu-id="a6d85-103">Tworzy nowy obiekt SqlUniqueKeyPolicy CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="a6d85-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="a6d85-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a6d85-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6d85-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a6d85-105">DESCRIPTION</span></span>
<span data-ttu-id="a6d85-106">Polecenie cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** tworzy nowy obiekt typu PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="a6d85-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="a6d85-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a6d85-107">EXAMPLES</span></span>

### <span data-ttu-id="a6d85-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6d85-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="a6d85-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a6d85-109">PARAMETERS</span></span>

### <span data-ttu-id="a6d85-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6d85-110">-DefaultProfile</span></span>
<span data-ttu-id="a6d85-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6d85-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6d85-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="a6d85-112">-UniqueKey</span></span>
<span data-ttu-id="a6d85-113">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a6d85-113">Database name.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6d85-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6d85-114">CommonParameters</span></span>
<span data-ttu-id="a6d85-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6d85-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6d85-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a6d85-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6d85-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6d85-117">INPUTS</span></span>

### <span data-ttu-id="a6d85-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a6d85-118">None</span></span>

## <span data-ttu-id="a6d85-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a6d85-119">OUTPUTS</span></span>

### <span data-ttu-id="a6d85-120">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a6d85-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="a6d85-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a6d85-121">NOTES</span></span>

## <span data-ttu-id="a6d85-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6d85-122">RELATED LINKS</span></span>
