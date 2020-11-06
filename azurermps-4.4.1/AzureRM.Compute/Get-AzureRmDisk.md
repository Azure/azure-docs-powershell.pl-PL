---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: e598c266f46815e7005c43e2d354ad8ece06efc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553371"
---
# <span data-ttu-id="43b76-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="43b76-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="43b76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43b76-102">SYNOPSIS</span></span>
<span data-ttu-id="43b76-103">Pobiera właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="43b76-103">Gets the properties of a disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43b76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43b76-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43b76-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43b76-105">DESCRIPTION</span></span>
<span data-ttu-id="43b76-106">Polecenie cmdlet **Get-AzureRmDisk** pobiera właściwości dysku.</span><span class="sxs-lookup"><span data-stu-id="43b76-106">The **Get-AzureRmDisk** cmdlet gets the properties of a disk.</span></span>

## <span data-ttu-id="43b76-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43b76-107">EXAMPLES</span></span>

### <span data-ttu-id="43b76-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="43b76-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="43b76-109">To polecenie pobiera właściwości dysku o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="43b76-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="43b76-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="43b76-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="43b76-111">To polecenie pobiera właściwości wszystkich dysków w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="43b76-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="43b76-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="43b76-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="43b76-113">To polecenie pobiera właściwości wszystkich dysków objętych abonamentem.</span><span class="sxs-lookup"><span data-stu-id="43b76-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="43b76-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43b76-114">PARAMETERS</span></span>

### <span data-ttu-id="43b76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43b76-115">-DefaultProfile</span></span>
<span data-ttu-id="43b76-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43b76-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43b76-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="43b76-117">-DiskName</span></span>
<span data-ttu-id="43b76-118">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="43b76-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="43b76-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43b76-119">-ResourceGroupName</span></span>
<span data-ttu-id="43b76-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="43b76-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="43b76-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43b76-121">CommonParameters</span></span>
<span data-ttu-id="43b76-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43b76-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43b76-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43b76-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43b76-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43b76-124">INPUTS</span></span>

### <span data-ttu-id="43b76-125">System. String</span><span class="sxs-lookup"><span data-stu-id="43b76-125">System.String</span></span>

## <span data-ttu-id="43b76-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43b76-126">OUTPUTS</span></span>

### <span data-ttu-id="43b76-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="43b76-127">System.Object</span></span>

## <span data-ttu-id="43b76-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43b76-128">NOTES</span></span>

## <span data-ttu-id="43b76-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43b76-129">RELATED LINKS</span></span>

