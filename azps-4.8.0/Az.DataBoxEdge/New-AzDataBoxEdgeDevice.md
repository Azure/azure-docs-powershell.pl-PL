---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 66c91c7a486638c01902f6091993143bb2e1a535
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223559"
---
# <span data-ttu-id="d34ca-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d34ca-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="d34ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d34ca-102">SYNOPSIS</span></span>
<span data-ttu-id="d34ca-103">Konfiguruje nowe urządzenie do krawędzi pola danych</span><span class="sxs-lookup"><span data-stu-id="d34ca-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="d34ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d34ca-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d34ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d34ca-105">DESCRIPTION</span></span>
<span data-ttu-id="d34ca-106">Polecenie cmdlet **New-AzDataBoxEdgeDevice** konfiguruje nowe urządzenie do krawędzi pola danych</span><span class="sxs-lookup"><span data-stu-id="d34ca-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="d34ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d34ca-107">EXAMPLES</span></span>

### <span data-ttu-id="d34ca-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d34ca-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="d34ca-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d34ca-109">PARAMETERS</span></span>

### <span data-ttu-id="d34ca-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d34ca-110">-AsJob</span></span>
<span data-ttu-id="d34ca-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d34ca-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d34ca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d34ca-112">-DefaultProfile</span></span>
<span data-ttu-id="d34ca-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d34ca-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d34ca-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d34ca-114">-Location</span></span>
<span data-ttu-id="d34ca-115">Lokalizacja urządzenia</span><span class="sxs-lookup"><span data-stu-id="d34ca-115">Location of the device</span></span>

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

### <span data-ttu-id="d34ca-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d34ca-116">-Name</span></span>
<span data-ttu-id="d34ca-117">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="d34ca-117">Resource Name</span></span>

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

### <span data-ttu-id="d34ca-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d34ca-118">-ResourceGroupName</span></span>
<span data-ttu-id="d34ca-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="d34ca-119">Resource Group Name</span></span>

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

### <span data-ttu-id="d34ca-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="d34ca-120">-Sku</span></span>
<span data-ttu-id="d34ca-121">Dostępne jednostki SKU to Edge, Brama</span><span class="sxs-lookup"><span data-stu-id="d34ca-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="d34ca-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d34ca-122">-Confirm</span></span>
<span data-ttu-id="d34ca-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d34ca-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d34ca-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d34ca-124">-WhatIf</span></span>
<span data-ttu-id="d34ca-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d34ca-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d34ca-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d34ca-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d34ca-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d34ca-127">CommonParameters</span></span>
<span data-ttu-id="d34ca-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d34ca-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d34ca-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d34ca-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d34ca-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d34ca-130">INPUTS</span></span>

### <span data-ttu-id="d34ca-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d34ca-131">None</span></span>

## <span data-ttu-id="d34ca-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d34ca-132">OUTPUTS</span></span>

### <span data-ttu-id="d34ca-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d34ca-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="d34ca-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d34ca-134">NOTES</span></span>

## <span data-ttu-id="d34ca-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d34ca-135">RELATED LINKS</span></span>
