---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmDisk.md
ms.openlocfilehash: 00d7368c49c86a9c089fef5bce3698b32eb65a74
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541895"
---
# <span data-ttu-id="c32be-101">Get-AzureRmDisk</span><span class="sxs-lookup"><span data-stu-id="c32be-101">Get-AzureRmDisk</span></span>

## <span data-ttu-id="c32be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c32be-102">SYNOPSIS</span></span>
<span data-ttu-id="c32be-103">Pobiera właściwości dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="c32be-103">Gets the properties of a Managed disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c32be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c32be-104">SYNTAX</span></span>

```
Get-AzureRmDisk [[-ResourceGroupName] <String>] [[-DiskName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c32be-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c32be-105">DESCRIPTION</span></span>
<span data-ttu-id="c32be-106">Polecenie cmdlet **Get-AzureRmDisk** pobiera właściwości dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="c32be-106">The **Get-AzureRmDisk** cmdlet gets the properties of a Managed disk.</span></span>

## <span data-ttu-id="c32be-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c32be-107">EXAMPLES</span></span>

### <span data-ttu-id="c32be-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c32be-108">Example 1</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01'
```

<span data-ttu-id="c32be-109">To polecenie pobiera właściwości dysku o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c32be-109">This command gets the properties of the disk named 'Disk01' in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c32be-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c32be-110">Example 2</span></span>
```
PS C:\> Get-AzureRmDisk -ResourceGroupName 'ResourceGroup01'
```

<span data-ttu-id="c32be-111">To polecenie pobiera właściwości wszystkich dysków w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="c32be-111">This command gets the properties of all disks in the resource group 'ResourceGroup01'.</span></span>

### <span data-ttu-id="c32be-112">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c32be-112">Example 3</span></span>
```
PS C:\> Get-AzureRmDisk
```

<span data-ttu-id="c32be-113">To polecenie pobiera właściwości wszystkich dysków objętych abonamentem.</span><span class="sxs-lookup"><span data-stu-id="c32be-113">This command gets the properties of all disks under the subscription.</span></span>

## <span data-ttu-id="c32be-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c32be-114">PARAMETERS</span></span>

### <span data-ttu-id="c32be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c32be-115">-DefaultProfile</span></span>
<span data-ttu-id="c32be-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c32be-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c32be-117">-Diskname</span><span class="sxs-lookup"><span data-stu-id="c32be-117">-DiskName</span></span>
<span data-ttu-id="c32be-118">Określa nazwę dysku.</span><span class="sxs-lookup"><span data-stu-id="c32be-118">Specifies the name of a disk.</span></span>

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

### <span data-ttu-id="c32be-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c32be-119">-ResourceGroupName</span></span>
<span data-ttu-id="c32be-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c32be-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="c32be-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c32be-121">CommonParameters</span></span>
<span data-ttu-id="c32be-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c32be-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c32be-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c32be-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c32be-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c32be-124">INPUTS</span></span>

### <span data-ttu-id="c32be-125">System. String</span><span class="sxs-lookup"><span data-stu-id="c32be-125">System.String</span></span>

## <span data-ttu-id="c32be-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c32be-126">OUTPUTS</span></span>

### <span data-ttu-id="c32be-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="c32be-127">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="c32be-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c32be-128">NOTES</span></span>

## <span data-ttu-id="c32be-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c32be-129">RELATED LINKS</span></span>
