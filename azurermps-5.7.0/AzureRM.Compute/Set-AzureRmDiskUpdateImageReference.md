---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 55a3a45cf22dd6558a9728a254531a0e01627e20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548147"
---
# <span data-ttu-id="0d4ff-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="0d4ff-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="0d4ff-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0d4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0d4ff-103">Ustawia właściwości odwołania obrazu w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d4ff-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0d4ff-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <DiskUpdate> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d4ff-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0d4ff-105">DESCRIPTION</span></span>
<span data-ttu-id="0d4ff-106">Polecenie cmdlet **Set-AzureRmDiskUpdateImageReference** ustawia właściwości odwołania obrazu w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="0d4ff-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0d4ff-107">EXAMPLES</span></span>

### <span data-ttu-id="0d4ff-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0d4ff-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="0d4ff-109">Pierwsze polecenie tworzy obiekt aktualizacji dysku lokalnego o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="0d4ff-110">Ustawia również typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="0d4ff-111">Drugie polecenie ustawia identyfikator obrazu i numer jednostki logicznej 0 dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="0d4ff-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="0d4ff-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="0d4ff-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0d4ff-113">PARAMETERS</span></span>

### <span data-ttu-id="0d4ff-114">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0d4ff-114">-DiskUpdate</span></span>
<span data-ttu-id="0d4ff-115">Określa obiekt aktualizacji dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-115">Specifies a local disk update object.</span></span>

```yaml
Type: DiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d4ff-116">-ID</span><span class="sxs-lookup"><span data-stu-id="0d4ff-116">-Id</span></span>
<span data-ttu-id="0d4ff-117">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="0d4ff-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="0d4ff-118">-Lun</span></span>
<span data-ttu-id="0d4ff-119">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="0d4ff-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="0d4ff-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0d4ff-120">-Confirm</span></span>
<span data-ttu-id="0d4ff-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d4ff-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d4ff-122">-WhatIf</span></span>
<span data-ttu-id="0d4ff-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d4ff-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d4ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d4ff-125">CommonParameters</span></span>
<span data-ttu-id="0d4ff-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d4ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d4ff-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d4ff-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d4ff-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0d4ff-128">INPUTS</span></span>

### <span data-ttu-id="0d4ff-129">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0d4ff-129">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="0d4ff-130">System. String. Nullable. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0d4ff-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="0d4ff-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0d4ff-131">OUTPUTS</span></span>

### <span data-ttu-id="0d4ff-132">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="0d4ff-132">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="0d4ff-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0d4ff-133">NOTES</span></span>

## <span data-ttu-id="0d4ff-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0d4ff-134">RELATED LINKS</span></span>

