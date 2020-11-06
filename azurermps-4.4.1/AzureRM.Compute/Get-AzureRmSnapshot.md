---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmSnapshot.md
ms.openlocfilehash: 98297d46416b23cd127e5ab5b65ce2fcfac38aa0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528254"
---
# <span data-ttu-id="f9062-101">Get-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="f9062-101">Get-AzureRmSnapshot</span></span>

## <span data-ttu-id="f9062-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9062-102">SYNOPSIS</span></span>
<span data-ttu-id="f9062-103">Pobiera właściwości migawki.</span><span class="sxs-lookup"><span data-stu-id="f9062-103">Gets the properties of a snapshot</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9062-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9062-104">SYNTAX</span></span>

```
Get-AzureRmSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9062-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f9062-105">DESCRIPTION</span></span>
<span data-ttu-id="f9062-106">Polecenie cmdlet **Get-AzureRmSnapshot** pobiera właściwości migawki.</span><span class="sxs-lookup"><span data-stu-id="f9062-106">The **Get-AzureRmSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="f9062-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9062-107">EXAMPLES</span></span>

### <span data-ttu-id="f9062-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9062-108">Example 1</span></span>
```
PS C:\> Get-AzureRmSnapshot
```

<span data-ttu-id="f9062-109">To polecenie pobiera właściwości wszystkich migawek subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f9062-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="f9062-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f9062-110">Example 2</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="f9062-111">To polecenie pobiera właściwości wszystkich migawek w grupie zasobów o nazwie "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="f9062-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="f9062-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f9062-112">Example 3</span></span>
```
PS C:\> Get-AzureRmSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="f9062-113">To polecenie pobiera właściwości migawki o nazwie "SnapshotName1" w grupie zasobów o nazwie "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="f9062-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="f9062-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9062-114">PARAMETERS</span></span>

### <span data-ttu-id="f9062-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9062-115">-DefaultProfile</span></span>
<span data-ttu-id="f9062-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9062-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9062-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9062-117">-ResourceGroupName</span></span>
<span data-ttu-id="f9062-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9062-118">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9062-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="f9062-119">-SnapshotName</span></span>
<span data-ttu-id="f9062-120">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="f9062-120">Specifies the name of a snapshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9062-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9062-121">CommonParameters</span></span>
<span data-ttu-id="f9062-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9062-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9062-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9062-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9062-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9062-124">INPUTS</span></span>

### <span data-ttu-id="f9062-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f9062-125">System.String</span></span>

## <span data-ttu-id="f9062-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9062-126">OUTPUTS</span></span>

### <span data-ttu-id="f9062-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="f9062-127">System.Object</span></span>

## <span data-ttu-id="f9062-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9062-128">NOTES</span></span>

## <span data-ttu-id="f9062-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9062-129">RELATED LINKS</span></span>

