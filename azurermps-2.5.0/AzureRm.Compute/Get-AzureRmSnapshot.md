---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermsnapshot
schema: 2.0.0
ms.openlocfilehash: 8133bfc8381f08e69afbd6bfbd3a25084e9eb2b9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898065"
---
# <span data-ttu-id="59e83-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="59e83-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="59e83-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59e83-102">SYNOPSIS</span></span>
<span data-ttu-id="59e83-103">Pobiera właściwości migawki.</span><span class="sxs-lookup"><span data-stu-id="59e83-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59e83-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59e83-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59e83-105">Opis</span><span class="sxs-lookup"><span data-stu-id="59e83-105">DESCRIPTION</span></span>
<span data-ttu-id="59e83-106">Polecenie cmdlet **Get-AzureRmSnapshot** pobiera właściwości migawki.</span><span class="sxs-lookup"><span data-stu-id="59e83-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="59e83-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59e83-107">EXAMPLES</span></span>

### <span data-ttu-id="59e83-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59e83-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="59e83-109">To polecenie pobiera właściwości wszystkich migawek subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="59e83-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="59e83-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="59e83-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="59e83-111">To polecenie pobiera właściwości wszystkich migawek w grupie zasobów o nazwie "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="59e83-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="59e83-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="59e83-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="59e83-113">To polecenie pobiera właściwości migawki o nazwie "SnapshotName1" w grupie zasobów o nazwie "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="59e83-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="59e83-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59e83-114">PARAMETERS</span></span>

### <span data-ttu-id="59e83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59e83-115">-DefaultProfile</span></span>
<span data-ttu-id="59e83-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59e83-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59e83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59e83-117">-ResourceGroupName</span></span>
<span data-ttu-id="59e83-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59e83-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="59e83-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="59e83-119">-SnapshotName</span></span>
<span data-ttu-id="59e83-120">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="59e83-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="59e83-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59e83-121">CommonParameters</span></span>
<span data-ttu-id="59e83-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59e83-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59e83-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59e83-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59e83-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59e83-124">INPUTS</span></span>

### <span data-ttu-id="59e83-125">System. String</span><span class="sxs-lookup"><span data-stu-id="59e83-125">System.String</span></span>

## <span data-ttu-id="59e83-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59e83-126">OUTPUTS</span></span>

### <span data-ttu-id="59e83-127">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="59e83-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="59e83-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59e83-128">NOTES</span></span>

## <span data-ttu-id="59e83-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59e83-129">RELATED LINKS</span></span>

