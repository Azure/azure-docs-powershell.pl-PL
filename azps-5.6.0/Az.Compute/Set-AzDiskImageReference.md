---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: aed0113b229d41665effd7904d2de2357b4b5d93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991460"
---
# <span data-ttu-id="e29f6-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="e29f6-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="e29f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e29f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e29f6-103">Ustawia właściwości odwołania do obrazu na obiekcie dysku.</span><span class="sxs-lookup"><span data-stu-id="e29f6-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="e29f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e29f6-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e29f6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e29f6-105">DESCRIPTION</span></span>
<span data-ttu-id="e29f6-106">Polecenie **cmdlet Set-AzFerenceImageReference** ustawia właściwości odwołania do obrazu na obiekcie dysku.</span><span class="sxs-lookup"><span data-stu-id="e29f6-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="e29f6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e29f6-107">EXAMPLES</span></span>

### <span data-ttu-id="e29f6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e29f6-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="e29f6-109">Pierwsze polecenie tworzy obiekt dysku lokalnego o rozmiarze 10 GB w Premium_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e29f6-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="e29f6-110">Ustawia także typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="e29f6-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="e29f6-111">Drugie polecenie ustawia identyfikator obrazu i jednostkę logiczną o numerze 0 obiektu dysku.</span><span class="sxs-lookup"><span data-stu-id="e29f6-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="e29f6-112">Ostatnie polecenie pobiera obiekt dysku i tworzy dysk o nazwie "Dysk01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="e29f6-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e29f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e29f6-113">PARAMETERS</span></span>

### <span data-ttu-id="e29f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e29f6-114">-DefaultProfile</span></span>
<span data-ttu-id="e29f6-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e29f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e29f6-116">— Dysk</span><span class="sxs-lookup"><span data-stu-id="e29f6-116">-Disk</span></span>
<span data-ttu-id="e29f6-117">Określa obiekt dysku lokalnego.</span><span class="sxs-lookup"><span data-stu-id="e29f6-117">Specifies a local disk object.</span></span>

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

### <span data-ttu-id="e29f6-118">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="e29f6-118">-Id</span></span>
<span data-ttu-id="e29f6-119">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="e29f6-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="e29f6-120">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="e29f6-120">-Lun</span></span>
<span data-ttu-id="e29f6-121">Określa numer jednostki logicznej (OWĄ).</span><span class="sxs-lookup"><span data-stu-id="e29f6-121">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="e29f6-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e29f6-122">-Confirm</span></span>
<span data-ttu-id="e29f6-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e29f6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e29f6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e29f6-124">-WhatIf</span></span>
<span data-ttu-id="e29f6-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e29f6-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e29f6-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e29f6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e29f6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e29f6-127">CommonParameters</span></span>
<span data-ttu-id="e29f6-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e29f6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e29f6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e29f6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e29f6-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e29f6-130">INPUTS</span></span>

### <span data-ttu-id="e29f6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="e29f6-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="e29f6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e29f6-132">System.String</span></span>

### <span data-ttu-id="e29f6-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="e29f6-133">System.Int32</span></span>

## <span data-ttu-id="e29f6-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e29f6-134">OUTPUTS</span></span>

### <span data-ttu-id="e29f6-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="e29f6-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="e29f6-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e29f6-136">NOTES</span></span>

## <span data-ttu-id="e29f6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e29f6-137">RELATED LINKS</span></span>
