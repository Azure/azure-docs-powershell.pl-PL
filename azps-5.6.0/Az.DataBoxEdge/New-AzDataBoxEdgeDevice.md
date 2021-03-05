---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: b7deb19377d893d28d5b5924acf8c49daf706907
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978682"
---
# <span data-ttu-id="f2084-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f2084-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f2084-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2084-102">SYNOPSIS</span></span>
<span data-ttu-id="f2084-103">Konfiguruje nowe urządzenie z krawędzią pola danych</span><span class="sxs-lookup"><span data-stu-id="f2084-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="f2084-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f2084-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2084-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f2084-105">DESCRIPTION</span></span>
<span data-ttu-id="f2084-106">Polecenie **cmdlet New-AzDataBoxEdgeDevice konfiguruje** nowe urządzenie Edge pola danych</span><span class="sxs-lookup"><span data-stu-id="f2084-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="f2084-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f2084-107">EXAMPLES</span></span>

### <span data-ttu-id="f2084-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f2084-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="f2084-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2084-109">PARAMETERS</span></span>

### <span data-ttu-id="f2084-110">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f2084-110">-AsJob</span></span>
<span data-ttu-id="f2084-111">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f2084-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2084-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2084-112">-DefaultProfile</span></span>
<span data-ttu-id="f2084-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2084-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2084-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f2084-114">-Location</span></span>
<span data-ttu-id="f2084-115">Lokalizacja urządzenia</span><span class="sxs-lookup"><span data-stu-id="f2084-115">Location of the device</span></span>

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

### <span data-ttu-id="f2084-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f2084-116">-Name</span></span>
<span data-ttu-id="f2084-117">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="f2084-117">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2084-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2084-118">-ResourceGroupName</span></span>
<span data-ttu-id="f2084-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f2084-119">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2084-120">- SKU</span><span class="sxs-lookup"><span data-stu-id="f2084-120">-Sku</span></span>
<span data-ttu-id="f2084-121">Dostępne jednostki SKU to Edge, Gateway</span><span class="sxs-lookup"><span data-stu-id="f2084-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="f2084-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2084-122">-Confirm</span></span>
<span data-ttu-id="f2084-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f2084-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2084-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2084-124">-WhatIf</span></span>
<span data-ttu-id="f2084-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2084-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2084-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f2084-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2084-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2084-127">CommonParameters</span></span>
<span data-ttu-id="f2084-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2084-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2084-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f2084-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2084-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2084-130">INPUTS</span></span>

### <span data-ttu-id="f2084-131">Brak</span><span class="sxs-lookup"><span data-stu-id="f2084-131">None</span></span>

## <span data-ttu-id="f2084-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2084-132">OUTPUTS</span></span>

### <span data-ttu-id="f2084-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="f2084-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="f2084-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f2084-134">NOTES</span></span>

## <span data-ttu-id="f2084-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2084-135">RELATED LINKS</span></span>
