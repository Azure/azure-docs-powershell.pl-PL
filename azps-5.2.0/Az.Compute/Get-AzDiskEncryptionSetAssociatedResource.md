---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzDiskEncryptionSetAssociatedResource.md
ms.openlocfilehash: f85b1ffb181a277e750d6f6f4a67ef55ad2a75bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332794"
---
# <span data-ttu-id="0e79e-101">Get-AzDiskEncryptionSetAssociatedResource</span><span class="sxs-lookup"><span data-stu-id="0e79e-101">Get-AzDiskEncryptionSetAssociatedResource</span></span>

## <span data-ttu-id="0e79e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e79e-102">SYNOPSIS</span></span>
<span data-ttu-id="0e79e-103">Pobiera listę zasobów skojarzonych z określonym zestawem szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="0e79e-103">Gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="0e79e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e79e-104">SYNTAX</span></span>

```
Get-AzDiskEncryptionSetAssociatedResource [-ResourceGroupName] <String> [-DiskEncryptionSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e79e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0e79e-105">DESCRIPTION</span></span>
<span data-ttu-id="0e79e-106">Polecenie cmdlet **Get-AzDiskEncryptionSetAssociatedResource** pobiera listę zasobów skojarzonych z określonym zestawem szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="0e79e-106">The **Get-AzDiskEncryptionSetAssociatedResource** cmdlet gets the list of resources associated with the specified disk encryption set.</span></span>

## <span data-ttu-id="0e79e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e79e-107">EXAMPLES</span></span>

### <span data-ttu-id="0e79e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0e79e-108">Example 1</span></span>
```powershell
PS C:\> Get-AzDiskEncryptionSetAssociatedResource -ResourceGroupName $RGname -DiskEncryptionSetName $diskEncryptionSetName

/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exampleDisk01
/subscriptions/xxxxx-xxx-xx/resourceGroups/exampleResourceGroup/providers/Microsoft.Compute/disks/exmapleDisk02
```

<span data-ttu-id="0e79e-109">Polecenie cmdlet umożliwia pobranie dwóch zasobów, "exampleDisk01" i "exampleDisk02", skojarzonych z określonym zestawem szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="0e79e-109">The cmdlet retrieves the two resources, 'exampleDisk01' and 'exampleDisk02', associated with the provided Disk Encryption Set</span></span>

## <span data-ttu-id="0e79e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e79e-110">PARAMETERS</span></span>

### <span data-ttu-id="0e79e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e79e-111">-DefaultProfile</span></span>
<span data-ttu-id="0e79e-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0e79e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e79e-113">-DiskEncryptionSetName</span><span class="sxs-lookup"><span data-stu-id="0e79e-113">-DiskEncryptionSetName</span></span>
<span data-ttu-id="0e79e-114">Nazwa zestawu szyfrowania dysków.</span><span class="sxs-lookup"><span data-stu-id="0e79e-114">Name of disk encryption set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e79e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e79e-115">-ResourceGroupName</span></span>
<span data-ttu-id="0e79e-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0e79e-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e79e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e79e-117">CommonParameters</span></span>
<span data-ttu-id="0e79e-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e79e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e79e-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0e79e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e79e-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e79e-120">INPUTS</span></span>

### <span data-ttu-id="0e79e-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0e79e-121">System.String</span></span>

## <span data-ttu-id="0e79e-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e79e-122">OUTPUTS</span></span>

### <span data-ttu-id="0e79e-123">System. URI []</span><span class="sxs-lookup"><span data-stu-id="0e79e-123">System.Uri[]</span></span>

## <span data-ttu-id="0e79e-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e79e-124">NOTES</span></span>

## <span data-ttu-id="0e79e-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e79e-125">RELATED LINKS</span></span>
