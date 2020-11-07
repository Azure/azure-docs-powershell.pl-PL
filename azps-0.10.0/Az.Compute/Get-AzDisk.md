---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzDisk.md
ms.openlocfilehash: 1da5ac8a6952e2a03367e84894f2069ba7ff250f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893814"
---
# <span data-ttu-id="973a3-101">Get-AzDisk</span><span class="sxs-lookup"><span data-stu-id="973a3-101">Get-AzDisk</span></span>

## <span data-ttu-id="973a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="973a3-102">SYNOPSIS</span></span>
<span data-ttu-id="973a3-103">Pobiera właściwości dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="973a3-103">Gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="973a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="973a3-104">SYNTAX</span></span>

```
Get-AzDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="973a3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="973a3-105">DESCRIPTION</span></span>
<span data-ttu-id="973a3-106">Polecenie cmdlet **Get-AzDisk** pobiera właściwości dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="973a3-106">The **Get-AzDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="973a3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="973a3-107">EXAMPLES</span></span>

### <span data-ttu-id="973a3-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="973a3-108">Example 1</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="973a3-109">To polecenie pobiera właściwości dysku o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="973a3-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="973a3-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="973a3-110">Example 2</span></span>
```
PS C:\> Get-AzDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="973a3-111">To polecenie pobiera właściwości wszystkich dysków w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="973a3-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="973a3-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="973a3-112">Example 3</span></span>
```
PS C:\> Get-AzDisk
```

<span data-ttu-id="973a3-113">To polecenie pobiera właściwości wszystkich dysków objętych abonamentem.</span><span class="sxs-lookup"><span data-stu-id="973a3-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="973a3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="973a3-114">PARAMETERS</span></span>

### <span data-ttu-id="973a3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="973a3-115">-DefaultProfile</span></span>
<span data-ttu-id="973a3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="973a3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="973a3-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="973a3-117">-DiskName</span></span>
<span data-ttu-id="973a3-118">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="973a3-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="973a3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="973a3-119">-ResourceGroupName</span></span>
<span data-ttu-id="973a3-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="973a3-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="973a3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="973a3-121">CommonParameters</span></span>
<span data-ttu-id="973a3-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="973a3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="973a3-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="973a3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="973a3-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="973a3-124">INPUTS</span></span>

### <span data-ttu-id="973a3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="973a3-125">System.String</span></span>

## <span data-ttu-id="973a3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="973a3-126">OUTPUTS</span></span>

### <span data-ttu-id="973a3-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="973a3-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="973a3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="973a3-128">NOTES</span></span>

## <span data-ttu-id="973a3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="973a3-129">RELATED LINKS</span></span>

