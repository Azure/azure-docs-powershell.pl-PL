---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196602"
---
# <span data-ttu-id="d8367-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d8367-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="d8367-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8367-102">SYNOPSIS</span></span>
<span data-ttu-id="d8367-103">Tworzy nowy kontener magazynu na koncie magazynu w programie Edge na urządzeniu.</span><span class="sxs-lookup"><span data-stu-id="d8367-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="d8367-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8367-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8367-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8367-105">DESCRIPTION</span></span>
<span data-ttu-id="d8367-106">Polecenie **cmdlet New-AzDataBoxEdgeStorageContainer** tworzy nowy kontener magazynu na koncie magazynu edge na urządzeniu z programem Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="d8367-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="d8367-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8367-107">EXAMPLES</span></span>

### <span data-ttu-id="d8367-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8367-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="d8367-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8367-109">PARAMETERS</span></span>

### <span data-ttu-id="d8367-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d8367-110">-AsJob</span></span>
<span data-ttu-id="d8367-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d8367-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8367-112">- DataFormat</span><span class="sxs-lookup"><span data-stu-id="d8367-112">-DataFormat</span></span>
<span data-ttu-id="d8367-113">Ustawianie formatu danych, np.: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="d8367-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8367-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8367-114">-DefaultProfile</span></span>
<span data-ttu-id="d8367-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8367-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8367-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d8367-116">-DeviceName</span></span>
<span data-ttu-id="d8367-117">Nazwa urządzenia</span><span class="sxs-lookup"><span data-stu-id="d8367-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8367-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d8367-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="d8367-119">Podaj nazwę istniejącego konta EdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d8367-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8367-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8367-120">-Name</span></span>
<span data-ttu-id="d8367-121">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="d8367-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8367-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8367-122">-ResourceGroupName</span></span>
<span data-ttu-id="d8367-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d8367-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8367-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8367-124">-Confirm</span></span>
<span data-ttu-id="d8367-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8367-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8367-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8367-126">-WhatIf</span></span>
<span data-ttu-id="d8367-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8367-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8367-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d8367-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8367-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8367-129">CommonParameters</span></span>
<span data-ttu-id="d8367-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8367-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8367-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8367-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8367-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8367-132">INPUTS</span></span>

### <span data-ttu-id="d8367-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d8367-133">System.String</span></span>

## <span data-ttu-id="d8367-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d8367-134">OUTPUTS</span></span>

### <span data-ttu-id="d8367-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d8367-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="d8367-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8367-136">NOTES</span></span>

## <span data-ttu-id="d8367-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8367-137">RELATED LINKS</span></span>
