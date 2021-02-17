---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 78a6c3bf85fae4fab9c5b9a06c366760b55804fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238709"
---
# <span data-ttu-id="adc81-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="adc81-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="adc81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adc81-102">SYNOPSIS</span></span>
<span data-ttu-id="adc81-103">Ustawia właściwości odwołania do obrazu na obiekcie dysku.</span><span class="sxs-lookup"><span data-stu-id="adc81-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="adc81-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="adc81-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adc81-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="adc81-105">DESCRIPTION</span></span>
<span data-ttu-id="adc81-106">Polecenie **cmdlet Set-AzFerenceImageReference** ustawia właściwości odwołania do obrazu na obiekcie dysku.</span><span class="sxs-lookup"><span data-stu-id="adc81-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="adc81-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="adc81-107">EXAMPLES</span></span>

### <span data-ttu-id="adc81-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="adc81-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="adc81-109">Pierwsze polecenie tworzy obiekt dysku lokalnego o rozmiarze 10 GB w Premium_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="adc81-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="adc81-110">Ustawia także typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="adc81-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="adc81-111">Drugie polecenie ustawia identyfikator obrazu i jednostkę logiczną o numerze 0 dla obiektu dysku.</span><span class="sxs-lookup"><span data-stu-id="adc81-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="adc81-112">Ostatnie polecenie pobiera obiekt dysku i tworzy dysk o nazwie "Dysk01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="adc81-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="adc81-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adc81-113">PARAMETERS</span></span>

### <span data-ttu-id="adc81-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adc81-114">-DefaultProfile</span></span>
<span data-ttu-id="adc81-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="adc81-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adc81-116">— Dysk</span><span class="sxs-lookup"><span data-stu-id="adc81-116">-Disk</span></span>
<span data-ttu-id="adc81-117">Określa obiekt dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="adc81-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="adc81-118">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="adc81-118">-Id</span></span>
<span data-ttu-id="adc81-119">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="adc81-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="adc81-120">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="adc81-120">-Lun</span></span>
<span data-ttu-id="adc81-121">Określa numer jednostki logicznej (OWĄ).</span><span class="sxs-lookup"><span data-stu-id="adc81-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="adc81-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="adc81-122">-Confirm</span></span>
<span data-ttu-id="adc81-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="adc81-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adc81-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adc81-124">-WhatIf</span></span>
<span data-ttu-id="adc81-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adc81-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="adc81-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="adc81-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="adc81-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adc81-127">CommonParameters</span></span>
<span data-ttu-id="adc81-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adc81-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adc81-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adc81-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adc81-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adc81-130">INPUTS</span></span>

### <span data-ttu-id="adc81-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="adc81-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="adc81-132">System.String</span><span class="sxs-lookup"><span data-stu-id="adc81-132">System.String</span></span>

### <span data-ttu-id="adc81-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="adc81-133">System.Int32</span></span>

## <span data-ttu-id="adc81-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adc81-134">OUTPUTS</span></span>

### <span data-ttu-id="adc81-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="adc81-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="adc81-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="adc81-136">NOTES</span></span>

## <span data-ttu-id="adc81-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adc81-137">RELATED LINKS</span></span>
