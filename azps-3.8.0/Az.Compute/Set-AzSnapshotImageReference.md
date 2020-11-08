---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azsnapshotimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzSnapshotImageReference.md
ms.openlocfilehash: deb122735b94ed8ac0de63330a9fbdb3ecac81d4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053856"
---
# <span data-ttu-id="250d5-101">Set-AzSnapshotImageReference</span><span class="sxs-lookup"><span data-stu-id="250d5-101">Set-AzSnapshotImageReference</span></span>

## <span data-ttu-id="250d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="250d5-102">SYNOPSIS</span></span>
<span data-ttu-id="250d5-103">Ustawia właściwości odwołania obrazu dla obiektu typu migawka.</span><span class="sxs-lookup"><span data-stu-id="250d5-103">Sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="250d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="250d5-104">SYNTAX</span></span>

```
Set-AzSnapshotImageReference [-Snapshot] <PSSnapshot> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="250d5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="250d5-105">DESCRIPTION</span></span>
<span data-ttu-id="250d5-106">Polecenie cmdlet **Set-AzSnapshotImageReference** ustawia właściwości odwołania obrazu w obiekcie Snapshot.</span><span class="sxs-lookup"><span data-stu-id="250d5-106">The **Set-AzSnapshotImageReference** cmdlet sets the image reference properties on a snapshot object.</span></span>

## <span data-ttu-id="250d5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="250d5-107">EXAMPLES</span></span>

### <span data-ttu-id="250d5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="250d5-108">Example 1</span></span>
```
PS C:\> $snapshotconfig = New-AzSnapshotConfig -SnapshotSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $snapshotconfig = Set-AzSnapshotImageReference -Snapshot $snapshotconfig -Id $image -Lun 0;
PS C:\> New-AzSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Snapshot $snapshotconfig;
```

<span data-ttu-id="250d5-109">Pierwsze polecenie tworzy obiekt Local Snapshot ze zdjęciem o rozmiarze 10GB w Premium_LRS typ konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="250d5-109">The first command creates a local snapshot object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="250d5-110">Ustawia również typ systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="250d5-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="250d5-111">Drugie polecenie ustawia identyfikator obrazu i numer jednostki logicznej 0 dla obiektu Snapshot.</span><span class="sxs-lookup"><span data-stu-id="250d5-111">The second command sets the image ID and the logical unit number 0 for the snapshot object.</span></span>
<span data-ttu-id="250d5-112">Ostatnie polecenie przyjmuje obiekt Snapshot i utworzy migawkę o nazwie "Snapshot01" w grupie zasobów "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="250d5-112">The last command takes the snapshot object and creates a snapshot with name 'Snapshot01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="250d5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="250d5-113">PARAMETERS</span></span>

### <span data-ttu-id="250d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="250d5-114">-DefaultProfile</span></span>
<span data-ttu-id="250d5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="250d5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="250d5-116">-ID</span><span class="sxs-lookup"><span data-stu-id="250d5-116">-Id</span></span>
<span data-ttu-id="250d5-117">Określa identyfikator.</span><span class="sxs-lookup"><span data-stu-id="250d5-117">Specifies the ID.</span></span>

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

### <span data-ttu-id="250d5-118">-LUN</span><span class="sxs-lookup"><span data-stu-id="250d5-118">-Lun</span></span>
<span data-ttu-id="250d5-119">Określa numer jednostki logicznej (LUN).</span><span class="sxs-lookup"><span data-stu-id="250d5-119">Specifies the logical unit number (LUN).</span></span>

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

### <span data-ttu-id="250d5-120">-Migawka</span><span class="sxs-lookup"><span data-stu-id="250d5-120">-Snapshot</span></span>
<span data-ttu-id="250d5-121">Określa lokalny obiekt migawki.</span><span class="sxs-lookup"><span data-stu-id="250d5-121">Specifies a local snapshot object.</span></span>

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

### <span data-ttu-id="250d5-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="250d5-122">-Confirm</span></span>
<span data-ttu-id="250d5-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="250d5-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="250d5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="250d5-124">-WhatIf</span></span>
<span data-ttu-id="250d5-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="250d5-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="250d5-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="250d5-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="250d5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="250d5-127">CommonParameters</span></span>
<span data-ttu-id="250d5-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="250d5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="250d5-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="250d5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="250d5-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="250d5-130">INPUTS</span></span>

### <span data-ttu-id="250d5-131">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="250d5-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

### <span data-ttu-id="250d5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="250d5-132">System.String</span></span>

### <span data-ttu-id="250d5-133">System. Int32</span><span class="sxs-lookup"><span data-stu-id="250d5-133">System.Int32</span></span>

## <span data-ttu-id="250d5-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="250d5-134">OUTPUTS</span></span>

### <span data-ttu-id="250d5-135">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSSnapshot</span><span class="sxs-lookup"><span data-stu-id="250d5-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSSnapshot</span></span>

## <span data-ttu-id="250d5-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="250d5-136">NOTES</span></span>

## <span data-ttu-id="250d5-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="250d5-137">RELATED LINKS</span></span>
