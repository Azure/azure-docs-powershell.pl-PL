---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 777216f6969e661721785601a21ee9604d5eec94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719365"
---
# <span data-ttu-id="380da-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="380da-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="380da-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="380da-102">SYNOPSIS</span></span>
<span data-ttu-id="380da-103">Ustawia właściwości odwołania obrazu w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="380da-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="380da-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="380da-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <PSDiskUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="380da-105">Opis</span><span class="sxs-lookup"><span data-stu-id="380da-105">DESCRIPTION</span></span>
<span data-ttu-id="380da-106">Polecenie cmdlet **Set-AzureRmDiskUpdateImageReference** ustawia właściwości odwołania obrazu w obiekcie aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="380da-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="380da-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="380da-107">EXAMPLES</span></span>

### <span data-ttu-id="380da-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="380da-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="380da-109">Pierwsze polecenie tworzy obiekt aktualizacji dysku lokalnego o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="380da-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="380da-110">Ustawia również typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="380da-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="380da-111">Drugie polecenie ustawia identyfikator obrazu i numer jednostki logicznej 0 dla obiektu aktualizacji dysku.</span><span class="sxs-lookup"><span data-stu-id="380da-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="380da-112">Ostatnie polecenie pobiera obiekt aktualizacji dysku i aktualizuje istniejący dysk o nazwie "Disk01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="380da-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="380da-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="380da-113">PARAMETERS</span></span>

### <span data-ttu-id="380da-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="380da-114">-DefaultProfile</span></span>
<span data-ttu-id="380da-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="380da-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="380da-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="380da-116">-DiskUpdate</span></span>
<span data-ttu-id="380da-117">Określa obiekt aktualizacji dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="380da-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="380da-118">-ID</span><span class="sxs-lookup"><span data-stu-id="380da-118">-Id</span></span>
<span data-ttu-id="380da-119">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="380da-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="380da-120">-LUN</span><span class="sxs-lookup"><span data-stu-id="380da-120">-Lun</span></span>
<span data-ttu-id="380da-121">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="380da-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="380da-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="380da-122">-Confirm</span></span>
<span data-ttu-id="380da-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380da-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="380da-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="380da-124">-WhatIf</span></span>
<span data-ttu-id="380da-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="380da-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="380da-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="380da-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="380da-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="380da-127">CommonParameters</span></span>
<span data-ttu-id="380da-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="380da-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="380da-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="380da-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="380da-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="380da-130">INPUTS</span></span>

### <span data-ttu-id="380da-131">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="380da-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="380da-132">System. String. Nullable. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="380da-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="380da-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="380da-133">OUTPUTS</span></span>

### <span data-ttu-id="380da-134">Microsoft. Azure. Management. COMPUTE. MODELES. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="380da-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="380da-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="380da-135">NOTES</span></span>

## <span data-ttu-id="380da-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="380da-136">RELATED LINKS</span></span>

