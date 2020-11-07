---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermdiskimagereference
schema: 2.0.0
ms.openlocfilehash: cd0a66d8f8d777df9a8ebc3791643234f0d15fb0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898774"
---
# <span data-ttu-id="ee2a0-101">Set-AzureRmDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="ee2a0-101">Set-AzureRmDiskImageReference</span></span>

## <span data-ttu-id="ee2a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee2a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ee2a0-103">Ustawia właściwości odwołania obrazu na obiekcie dysk.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-103">Sets the image reference properties on a disk object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee2a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee2a0-104">SYNTAX</span></span>

```
Set-AzureRmDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee2a0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee2a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ee2a0-106">Polecenie cmdlet **Set-AzureRmDiskImageReference** ustawia właściwości odwołania obrazu na obiekcie dysku.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-106">The **Set-AzureRmDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="ee2a0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee2a0-107">EXAMPLES</span></span>

### <span data-ttu-id="ee2a0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ee2a0-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzureRmDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzureRmDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="ee2a0-109">Pierwsze polecenie tworzy lokalny obiekt dyskowy z rozmiarem konta magazynu Premium_LRSgo o rozmiarze 10GB.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="ee2a0-110">Ustawia również typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="ee2a0-111">Drugie polecenie ustawia identyfikator obrazu i numer jednostki logicznej 0 dla obiektu dysk.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="ee2a0-112">Ostatnie polecenie pobiera obiekt dysk i tworzy dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="ee2a0-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="ee2a0-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee2a0-113">PARAMETERS</span></span>

### <span data-ttu-id="ee2a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee2a0-114">-DefaultProfile</span></span>
<span data-ttu-id="ee2a0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee2a0-116">— Dysk</span><span class="sxs-lookup"><span data-stu-id="ee2a0-116">-Disk</span></span>
<span data-ttu-id="ee2a0-117">Określa lokalny obiekt dyskowy.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-117">Specifies a local disk object.</span></span>

```yaml
Type: PSDisk
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee2a0-118">-ID</span><span class="sxs-lookup"><span data-stu-id="ee2a0-118">-Id</span></span>
<span data-ttu-id="ee2a0-119">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="ee2a0-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="ee2a0-120">-Lun</span></span>
<span data-ttu-id="ee2a0-121">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="ee2a0-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee2a0-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ee2a0-122">-Confirm</span></span>
<span data-ttu-id="ee2a0-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2a0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee2a0-124">-WhatIf</span></span>
<span data-ttu-id="ee2a0-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee2a0-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee2a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee2a0-127">CommonParameters</span></span>
<span data-ttu-id="ee2a0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee2a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee2a0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee2a0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee2a0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee2a0-130">INPUTS</span></span>

### <span data-ttu-id="ee2a0-131">Microsoft. Azure. Management. COMPUTE. modele. Disk</span><span class="sxs-lookup"><span data-stu-id="ee2a0-131">Microsoft.Azure.Management.Compute.Models.Disk</span></span>
<span data-ttu-id="ee2a0-132">System. String. Nullable. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ee2a0-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="ee2a0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee2a0-133">OUTPUTS</span></span>

### <span data-ttu-id="ee2a0-134">Microsoft. Azure. Management. COMPUTE. modele. Disk</span><span class="sxs-lookup"><span data-stu-id="ee2a0-134">Microsoft.Azure.Management.Compute.Models.Disk</span></span>

## <span data-ttu-id="ee2a0-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee2a0-135">NOTES</span></span>

## <span data-ttu-id="ee2a0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee2a0-136">RELATED LINKS</span></span>

