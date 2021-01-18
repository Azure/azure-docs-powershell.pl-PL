---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503811"
---
# <span data-ttu-id="37e86-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="37e86-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="37e86-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37e86-102">SYNOPSIS</span></span>
<span data-ttu-id="37e86-103">Tworzy nowy obiekt SqlUniqueKeyPolicy CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="37e86-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="37e86-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37e86-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="37e86-105">Opis</span><span class="sxs-lookup"><span data-stu-id="37e86-105">DESCRIPTION</span></span>
<span data-ttu-id="37e86-106">Polecenie cmdlet **New-AzCosmosDBSqlUniqueKeyPolicy** tworzy nowy obiekt typu PSSqlUniqueKeyPolicy.</span><span class="sxs-lookup"><span data-stu-id="37e86-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="37e86-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37e86-107">EXAMPLES</span></span>

### <span data-ttu-id="37e86-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37e86-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="37e86-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37e86-109">PARAMETERS</span></span>

### <span data-ttu-id="37e86-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37e86-110">-DefaultProfile</span></span>
<span data-ttu-id="37e86-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37e86-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37e86-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="37e86-112">-UniqueKey</span></span>
<span data-ttu-id="37e86-113">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="37e86-113">Database name.</span></span>

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

### <span data-ttu-id="37e86-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37e86-114">CommonParameters</span></span>
<span data-ttu-id="37e86-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37e86-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37e86-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="37e86-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37e86-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37e86-117">INPUTS</span></span>

### <span data-ttu-id="37e86-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="37e86-118">None</span></span>

## <span data-ttu-id="37e86-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37e86-119">OUTPUTS</span></span>

### <span data-ttu-id="37e86-120">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="37e86-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="37e86-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37e86-121">NOTES</span></span>

## <span data-ttu-id="37e86-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37e86-122">RELATED LINKS</span></span>
