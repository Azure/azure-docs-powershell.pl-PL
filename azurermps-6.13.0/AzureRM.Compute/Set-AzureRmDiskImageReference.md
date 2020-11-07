---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmDiskImageReference.md
ms.openlocfilehash: e544007d8e23e20ed311f07eb33f98a5e2d6a409
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717464"
---
# <span data-ttu-id="ad5f0-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="ad5f0-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="ad5f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad5f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5f0-103">Ustawia właściwości odwołania obrazu na obiekcie dysk.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad5f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad5f0-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad5f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ad5f0-105">DESCRIPTION</span></span>
<span data-ttu-id="ad5f0-106">Polecenie cmdlet **Set-AzureRmDiskImageReference** ustawia właściwości odwołania obrazu na obiekcie dysku.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="ad5f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad5f0-107">EXAMPLES</span></span>

### <span data-ttu-id="ad5f0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad5f0-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ad5f0-109">Pierwsze polecenie tworzy lokalny obiekt dyskowy z rozmiarem konta magazynu Premium_LRSgo o rozmiarze 10GB.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ad5f0-110">Ustawia również typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="ad5f0-111">Drugie polecenie ustawia identyfikator obrazu i numer jednostki logicznej 0 dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="ad5f0-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ad5f0-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ad5f0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad5f0-113">PARAMETERS</span></span>

### <span data-ttu-id="ad5f0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5f0-114">-DefaultProfile</span></span>
<span data-ttu-id="ad5f0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad5f0-116">— Dysk</span><span class="sxs-lookup"><span data-stu-id="ad5f0-116">-Disk</span></span>
<span data-ttu-id="ad5f0-117">Określa lokalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5f0-118">-ID</span><span class="sxs-lookup"><span data-stu-id="ad5f0-118">-Id</span></span>
<span data-ttu-id="ad5f0-119">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="ad5f0-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="ad5f0-120">-Lun</span></span>
<span data-ttu-id="ad5f0-121">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="ad5f0-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad5f0-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad5f0-122">-Confirm</span></span>
<span data-ttu-id="ad5f0-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5f0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad5f0-124">-WhatIf</span></span>
<span data-ttu-id="ad5f0-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad5f0-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5f0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5f0-127">CommonParameters</span></span>
<span data-ttu-id="ad5f0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad5f0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5f0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad5f0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5f0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad5f0-130">INPUTS</span></span>

### <span data-ttu-id="ad5f0-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="ad5f0-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="ad5f0-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ad5f0-132">System.String</span></span>

### <span data-ttu-id="ad5f0-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="ad5f0-133">System.Int32</span></span>

## <span data-ttu-id="ad5f0-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad5f0-134">OUTPUTS</span></span>

### <span data-ttu-id="ad5f0-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDISK</span><span class="sxs-lookup"><span data-stu-id="ad5f0-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="ad5f0-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad5f0-136">NOTES</span></span>

## <span data-ttu-id="ad5f0-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad5f0-137">RELATED LINKS</span></span>
