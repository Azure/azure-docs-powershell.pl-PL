---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azsnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzSnapshot.md
ms.openlocfilehash: 25395cca287e7f711d5e124ab12919a0b5c01ce4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893813"
---
# <span data-ttu-id="eb92d-101">Get-AzSnapshot</span><span class="sxs-lookup"><span data-stu-id="eb92d-101">Get-AzSnapshot</span></span>

## <span data-ttu-id="eb92d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb92d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb92d-103">Pobiera właściwości migawki.</span><span class="sxs-lookup"><span data-stu-id="eb92d-103">Gets the properties of a snapshot</span></span>

## <span data-ttu-id="eb92d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb92d-104">SYNTAX</span></span>

```
Get-AzSnapshot [[-ResourceGroupName] <String>] [[-SnapshotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb92d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="eb92d-105">DESCRIPTION</span></span>
<span data-ttu-id="eb92d-106">Polecenie cmdlet **Get-AzSnapshot** pobiera właściwości migawki.</span><span class="sxs-lookup"><span data-stu-id="eb92d-106">The **Get-AzSnapshot** cmdlet gets the properties of a snapshot.</span></span>

## <span data-ttu-id="eb92d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb92d-107">EXAMPLES</span></span>

### <span data-ttu-id="eb92d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb92d-108">Example 1</span></span>
```
PS C:\> Get-AzSnapshot
```

<span data-ttu-id="eb92d-109">To polecenie pobiera właściwości wszystkich migawek subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="eb92d-109">This command gets the properties of all snapshots of the subscription.</span></span>

### <span data-ttu-id="eb92d-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="eb92d-110">Example 2</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1"
```

<span data-ttu-id="eb92d-111">To polecenie pobiera właściwości wszystkich migawek w grupie zasobów o nazwie "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="eb92d-111">This command gets the properties of all snapshots in the resource group named "ResourceGroupName1"</span></span>

### <span data-ttu-id="eb92d-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="eb92d-112">Example 3</span></span>
```
PS C:\> Get-AzSnapshot -ResourceGroupName "ResourceGroupName1" -SnapshotName "SnapshotName1"
```

<span data-ttu-id="eb92d-113">To polecenie pobiera właściwości migawki o nazwie "SnapshotName1" w grupie zasobów o nazwie "ResourceGroupName1".</span><span class="sxs-lookup"><span data-stu-id="eb92d-113">This command gets the properties of the snapshot named "SnapshotName1" in the resource group named "ResourceGroupName1"</span></span>

## <span data-ttu-id="eb92d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb92d-114">PARAMETERS</span></span>

### <span data-ttu-id="eb92d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb92d-115">-DefaultProfile</span></span>
<span data-ttu-id="eb92d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb92d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb92d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb92d-117">-ResourceGroupName</span></span>
<span data-ttu-id="eb92d-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb92d-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="eb92d-119">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="eb92d-119">-SnapshotName</span></span>
<span data-ttu-id="eb92d-120">Określa nazwę migawki.</span><span class="sxs-lookup"><span data-stu-id="eb92d-120">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="eb92d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb92d-121">CommonParameters</span></span>
<span data-ttu-id="eb92d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb92d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb92d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb92d-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb92d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb92d-124">INPUTS</span></span>

### <span data-ttu-id="eb92d-125">System. String</span><span class="sxs-lookup"><span data-stu-id="eb92d-125">System.String</span></span>

## <span data-ttu-id="eb92d-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb92d-126">OUTPUTS</span></span>

### <span data-ttu-id="eb92d-127">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="eb92d-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="eb92d-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb92d-128">NOTES</span></span>

## <span data-ttu-id="eb92d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb92d-129">RELATED LINKS</span></span>

