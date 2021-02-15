---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177482"
---
# <span data-ttu-id="025bc-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="025bc-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="025bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="025bc-102">SYNOPSIS</span></span>
<span data-ttu-id="025bc-103">Ustawia właściwości odwołania do obrazu w obiekcie migawki.</span><span class="sxs-lookup"><span data-stu-id="025bc-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="025bc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="025bc-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="025bc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="025bc-105">DESCRIPTION</span></span>
<span data-ttu-id="025bc-106">Polecenie **cmdlet Set-AzSnapshotImageReference** ustawia właściwości odwołania do obrazu w obiekcie migawki.</span><span class="sxs-lookup"><span data-stu-id="025bc-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="025bc-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="025bc-107">EXAMPLES</span></span>

### <span data-ttu-id="025bc-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="025bc-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="025bc-109">Pierwsze polecenie tworzy obiekt migawki lokalnej o rozmiarze 10 GB w Premium_LRS typu konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="025bc-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="025bc-110">Ustawia także typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="025bc-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="025bc-111">Drugie polecenie ustawia identyfikator obrazu i jednostkę logiczną o numerze 0 obiektu migawki.</span><span class="sxs-lookup"><span data-stu-id="025bc-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="025bc-112">Ostatnie polecenie pobiera obiekt migawki i tworzy migawkę o nazwie "Migawka01" w grupie zasobów "Grupa Zasobów01".</span><span class="sxs-lookup"><span data-stu-id="025bc-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="025bc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="025bc-113">PARAMETERS</span></span>

### <span data-ttu-id="025bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="025bc-114">-DefaultProfile</span></span>
<span data-ttu-id="025bc-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="025bc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="025bc-116">— Id</span><span class="sxs-lookup"><span data-stu-id="025bc-116">-Id</span></span>
<span data-ttu-id="025bc-117">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="025bc-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="025bc-118">-Logicznej</span><span class="sxs-lookup"><span data-stu-id="025bc-118">-Lun</span></span>
<span data-ttu-id="025bc-119">Określa numer jednostki logicznej (OWĄ).</span><span class="sxs-lookup"><span data-stu-id="025bc-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="025bc-120">— Migawka</span><span class="sxs-lookup"><span data-stu-id="025bc-120">-Snapshot</span></span>
<span data-ttu-id="025bc-121">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="025bc-121">Specifies a local snapshot object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="025bc-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="025bc-122">-Confirm</span></span>
<span data-ttu-id="025bc-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="025bc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="025bc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="025bc-124">-WhatIf</span></span>
<span data-ttu-id="025bc-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="025bc-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="025bc-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="025bc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="025bc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="025bc-127">CommonParameters</span></span>
<span data-ttu-id="025bc-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="025bc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="025bc-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="025bc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="025bc-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="025bc-130">INPUTS</span></span>

### <span data-ttu-id="025bc-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="025bc-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="025bc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="025bc-132">System.String</span></span>

### <span data-ttu-id="025bc-133">System.Int32</span><span class="sxs-lookup"><span data-stu-id="025bc-133">System.Int32</span></span>

## <span data-ttu-id="025bc-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="025bc-134">OUTPUTS</span></span>

### <span data-ttu-id="025bc-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="025bc-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="025bc-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="025bc-136">NOTES</span></span>

## <span data-ttu-id="025bc-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="025bc-137">RELATED LINKS</span></span>
