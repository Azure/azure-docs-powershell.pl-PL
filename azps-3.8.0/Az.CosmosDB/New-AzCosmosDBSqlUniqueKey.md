---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052599"
---
# <span data-ttu-id="efc76-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="efc76-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="efc76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="efc76-102">SYNOPSIS</span></span>
<span data-ttu-id="efc76-103">Tworzy nowy obiekt UniqueKey SQL CosmosDB.</span><span class="sxs-lookup"><span data-stu-id="efc76-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="efc76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="efc76-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efc76-105">Opis</span><span class="sxs-lookup"><span data-stu-id="efc76-105">DESCRIPTION</span></span>
<span data-ttu-id="efc76-106">Polecenie cmdlet **New-AzCosmosDBSqlUniqueKey** tworzy nowy obiekt typu PSUniqueKey.</span><span class="sxs-lookup"><span data-stu-id="efc76-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="efc76-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="efc76-107">EXAMPLES</span></span>

### <span data-ttu-id="efc76-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="efc76-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="efc76-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="efc76-109">PARAMETERS</span></span>

### <span data-ttu-id="efc76-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efc76-110">-DefaultProfile</span></span>
<span data-ttu-id="efc76-111">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="efc76-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efc76-112">-Path</span><span class="sxs-lookup"><span data-stu-id="efc76-112">-Path</span></span>
<span data-ttu-id="efc76-113">Tablica ciągów wartości ścieżki</span><span class="sxs-lookup"><span data-stu-id="efc76-113">Array of string of path values</span></span>

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

### <span data-ttu-id="efc76-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc76-114">CommonParameters</span></span>
<span data-ttu-id="efc76-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc76-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc76-116">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="efc76-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc76-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="efc76-117">INPUTS</span></span>

### <span data-ttu-id="efc76-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="efc76-118">None</span></span>

## <span data-ttu-id="efc76-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="efc76-119">OUTPUTS</span></span>

### <span data-ttu-id="efc76-120">Microsoft. Azure. Commands. CosmosDB. models. PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="efc76-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="efc76-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="efc76-121">NOTES</span></span>

## <span data-ttu-id="efc76-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="efc76-122">RELATED LINKS</span></span>
