---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 9f4d2c4e6321d36079cf4c5e87747863c8dc51c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546883"
---
# <span data-ttu-id="1370f-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="1370f-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="1370f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1370f-102">SYNOPSIS</span></span>
<span data-ttu-id="1370f-103">Pobiera właściwości migawki.</span><span class="sxs-lookup"><span data-stu-id="1370f-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1370f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1370f-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="1370f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1370f-105">DESCRIPTION</span></span>
<span data-ttu-id="1370f-106">Polecenie cmdlet **Get-AzureRmSnapshot** pobiera właściwości migawki.</span><span class="sxs-lookup"><span data-stu-id="1370f-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="1370f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1370f-107">EXAMPLES</span></span>

### <span data-ttu-id="1370f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1370f-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="1370f-109">To polecenie pobiera właściwości wszystkich migawek subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1370f-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="1370f-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1370f-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="1370f-111">To polecenie pobiera właściwości wszystkich migawek w grupie zasobów o nazwie "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="1370f-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="1370f-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="1370f-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="1370f-113">To polecenie pobiera właściwości migawki o nazwie "SnapshotName1" w grupie zasobów o nazwie "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="1370f-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="1370f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1370f-114">PARAMETERS</span></span>

### <span data-ttu-id="1370f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1370f-115">-ResourceGroupName</span></span>
<span data-ttu-id="1370f-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1370f-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-117">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="1370f-117">-SnapshotName</span></span>
<span data-ttu-id="1370f-118">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="1370f-118">Specifies the name of a snapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1370f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1370f-119">CommonParameters</span></span>
<span data-ttu-id="1370f-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1370f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1370f-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1370f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1370f-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1370f-122">INPUTS</span></span>

### <span data-ttu-id="1370f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="1370f-123">System.String</span></span>

## <span data-ttu-id="1370f-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1370f-124">OUTPUTS</span></span>

### <span data-ttu-id="1370f-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="1370f-125">System.Object</span></span>

## <span data-ttu-id="1370f-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1370f-126">NOTES</span></span>

## <span data-ttu-id="1370f-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1370f-127">RELATED LINKS</span></span>

