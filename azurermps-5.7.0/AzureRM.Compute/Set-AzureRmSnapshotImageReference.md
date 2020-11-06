---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmSnapshotImageReference.md
ms.openlocfilehash: 262184f82aa169b5e76d3b875d0e3ba27db4da38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525293"
---
# <span data-ttu-id="45ef9-101">Set-AzureRmSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="45ef9-101">Set-AzureRmSnapshotImageReference</span></span>

## <span data-ttu-id="45ef9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="45ef9-103">Ustawia właściwości odwołania obrazu dla obiektu typu migawka.</span><span class="sxs-lookup"><span data-stu-id="45ef9-103">Sets the image reference properties on a snapshot object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45ef9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45ef9-104">SYNTAX</span></span>

```
Set-AzureRmSnapshotImageReference [-Snapshot] <Snapshot> [[-Id] <String>] [[-Lun] <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45ef9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="45ef9-105">DESCRIPTION</span></span>
<span data-ttu-id="45ef9-106">Polecenie cmdlet **Set-AzureRmSnapshotImageReference** ustawia właściwości odwołania obrazu w obiekcie Snapshot.</span><span class="sxs-lookup"><span data-stu-id="45ef9-106">The **Set-AzureRmSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="45ef9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45ef9-107">EXAMPLES</span></span>

### <span data-ttu-id="45ef9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45ef9-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzureRmSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzureRmSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="45ef9-109">Pierwsze polecenie tworzy obiekt Local Snapshot ze zdjęciem o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="45ef9-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="45ef9-110">Ustawia również typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="45ef9-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="45ef9-111">Drugie polecenie ustawia identyfikator obrazu i numer jednostki logicznej 0 dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="45ef9-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="45ef9-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="45ef9-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="45ef9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45ef9-113">PARAMETERS</span></span>

### <span data-ttu-id="45ef9-114">-ID</span><span class="sxs-lookup"><span data-stu-id="45ef9-114">-Id</span></span>
<span data-ttu-id="45ef9-115">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="45ef9-115">Specifies the ID.</span></span>

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

### <span data-ttu-id="45ef9-116">-LUN</span><span class="sxs-lookup"><span data-stu-id="45ef9-116">-Lun</span></span>
<span data-ttu-id="45ef9-117">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="45ef9-117">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="45ef9-118">-Migawka</span><span class="sxs-lookup"><span data-stu-id="45ef9-118">-Snapshot</span></span>
<span data-ttu-id="45ef9-119">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="45ef9-119">Specifies a local snapshot object.</span></span>

```yaml
Type: Snapshot
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45ef9-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45ef9-120">-Confirm</span></span>
<span data-ttu-id="45ef9-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ef9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ef9-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45ef9-122">-WhatIf</span></span>
<span data-ttu-id="45ef9-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ef9-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45ef9-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45ef9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ef9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ef9-125">CommonParameters</span></span>
<span data-ttu-id="45ef9-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ef9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ef9-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45ef9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ef9-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45ef9-128">INPUTS</span></span>

### <span data-ttu-id="45ef9-129">Microsoft. Azure. Management. COMPUTE. models. snapshot</span><span class="sxs-lookup"><span data-stu-id="45ef9-129">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>
<span data-ttu-id="45ef9-130">System. String. Nullable. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="45ef9-130">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="45ef9-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45ef9-131">OUTPUTS</span></span>

### <span data-ttu-id="45ef9-132">Microsoft. Azure. Management. COMPUTE. models. snapshot</span><span class="sxs-lookup"><span data-stu-id="45ef9-132">Microsoft.Azure.Management.Compute.Models.Snapshot</span></span>

## <span data-ttu-id="45ef9-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45ef9-133">NOTES</span></span>

## <span data-ttu-id="45ef9-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45ef9-134">RELATED LINKS</span></span>

