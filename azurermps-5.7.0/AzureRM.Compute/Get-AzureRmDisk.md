---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e34016b3bc7677c9591c07e54dd42a88a820d44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546891"
---
# <span data-ttu-id="ee4a1-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="ee4a1-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="ee4a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee4a1-102">SYNOPSIS</span></span>
<span data-ttu-id="ee4a1-103">Pobiera właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="ee4a1-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee4a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee4a1-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="ee4a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee4a1-105">DESCRIPTION</span></span>
<span data-ttu-id="ee4a1-106">Polecenie cmdlet **Get-AzureRmDisk** pobiera właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="ee4a1-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="ee4a1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee4a1-107">EXAMPLES</span></span>

### <span data-ttu-id="ee4a1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee4a1-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="ee4a1-109">To polecenie pobiera właściwości dysku o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ee4a1-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ee4a1-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ee4a1-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="ee4a1-111">To polecenie pobiera właściwości wszystkich dysków w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ee4a1-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="ee4a1-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ee4a1-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="ee4a1-113">To polecenie pobiera właściwości wszystkich dysków objętych abonamentem.</span><span class="sxs-lookup"><span data-stu-id="ee4a1-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="ee4a1-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee4a1-114">PARAMETERS</span></span>

### <span data-ttu-id="ee4a1-115">-Diskname</span><span class="sxs-lookup"><span data-stu-id="ee4a1-115">-DiskName</span></span>
<span data-ttu-id="ee4a1-116">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="ee4a1-116">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="ee4a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee4a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee4a1-118">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ee4a1-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ee4a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee4a1-119">CommonParameters</span></span>
<span data-ttu-id="ee4a1-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee4a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee4a1-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee4a1-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee4a1-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee4a1-122">INPUTS</span></span>

### <span data-ttu-id="ee4a1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ee4a1-123">System.String</span></span>

## <span data-ttu-id="ee4a1-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee4a1-124">OUTPUTS</span></span>

### <span data-ttu-id="ee4a1-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span><span class="sxs-lookup"><span data-stu-id="ee4a1-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskList</span></span>

## <span data-ttu-id="ee4a1-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee4a1-126">NOTES</span></span>

## <span data-ttu-id="ee4a1-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee4a1-127">RELATED LINKS</span></span>

