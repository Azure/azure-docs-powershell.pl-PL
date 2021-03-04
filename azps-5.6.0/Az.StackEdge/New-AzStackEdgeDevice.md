---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: 1ad2719ae67c96088dde968d96ca7104436083e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981994"
---
# <span data-ttu-id="b2824-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b2824-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="b2824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2824-102">SYNOPSIS</span></span>
<span data-ttu-id="b2824-103">Konfiguruje nowe urządzenie Stack Edge</span><span class="sxs-lookup"><span data-stu-id="b2824-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="b2824-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2824-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2824-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2824-105">DESCRIPTION</span></span>
<span data-ttu-id="b2824-106">Polecenie **cmdlet New-AzStackEdgeDevice konfiguruje** nowe urządzenie Stack Edge</span><span class="sxs-lookup"><span data-stu-id="b2824-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="b2824-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2824-107">EXAMPLES</span></span>

### <span data-ttu-id="b2824-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2824-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="b2824-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2824-109">PARAMETERS</span></span>

### <span data-ttu-id="b2824-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b2824-110">-AsJob</span></span>
<span data-ttu-id="b2824-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b2824-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b2824-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2824-112">-DefaultProfile</span></span>
<span data-ttu-id="b2824-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2824-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2824-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b2824-114">-Location</span></span>
<span data-ttu-id="b2824-115">Lokalizacja urządzenia</span><span class="sxs-lookup"><span data-stu-id="b2824-115">Location of the device</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2824-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b2824-116">-Name</span></span>
<span data-ttu-id="b2824-117">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="b2824-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeviceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2824-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2824-118">-ResourceGroupName</span></span>
<span data-ttu-id="b2824-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="b2824-119">Resource Group Name</span></span>

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

### <span data-ttu-id="b2824-120">- SKU</span><span class="sxs-lookup"><span data-stu-id="b2824-120">-Sku</span></span>
<span data-ttu-id="b2824-121">Dostępne jednostki SKU to Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="b2824-121">Available Skus are Edge, Gateway</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2824-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b2824-122">-Confirm</span></span>
<span data-ttu-id="b2824-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b2824-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2824-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2824-124">-WhatIf</span></span>
<span data-ttu-id="b2824-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2824-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2824-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b2824-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2824-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2824-127">CommonParameters</span></span>
<span data-ttu-id="b2824-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2824-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2824-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2824-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2824-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2824-130">INPUTS</span></span>

### <span data-ttu-id="b2824-131">Brak</span><span class="sxs-lookup"><span data-stu-id="b2824-131">None</span></span>

## <span data-ttu-id="b2824-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2824-132">OUTPUTS</span></span>

### <span data-ttu-id="b2824-133">Microsoft.Azure.PowerShell.Cmdlet.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="b2824-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="b2824-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2824-134">NOTES</span></span>

## <span data-ttu-id="b2824-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2824-135">RELATED LINKS</span></span>
