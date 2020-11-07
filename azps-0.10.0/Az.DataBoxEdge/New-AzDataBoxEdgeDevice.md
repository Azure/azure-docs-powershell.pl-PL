---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 353d4ca1e5f5eebd1cda1ec22d801a73db239963
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893245"
---
# <span data-ttu-id="a8349-101">New-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a8349-101">New-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a8349-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8349-102">SYNOPSIS</span></span>
<span data-ttu-id="a8349-103">Konfiguruje nowe urządzenie do krawędzi pola danych</span><span class="sxs-lookup"><span data-stu-id="a8349-103">Configures a new Data Box Edge device</span></span>

## <span data-ttu-id="a8349-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8349-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8349-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a8349-105">DESCRIPTION</span></span>
<span data-ttu-id="a8349-106">Polecenie cmdlet **New-AzDataBoxEdgeDevice** konfiguruje nowe urządzenie do krawędzi pola danych</span><span class="sxs-lookup"><span data-stu-id="a8349-106">The **New-AzDataBoxEdgeDevice** cmdlet configures a new Data Box Edge device</span></span>

## <span data-ttu-id="a8349-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8349-107">EXAMPLES</span></span>

### <span data-ttu-id="a8349-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a8349-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="a8349-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8349-109">PARAMETERS</span></span>

### <span data-ttu-id="a8349-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8349-110">-AsJob</span></span>
<span data-ttu-id="a8349-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a8349-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8349-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8349-112">-DefaultProfile</span></span>
<span data-ttu-id="a8349-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8349-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8349-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a8349-114">-Location</span></span>
<span data-ttu-id="a8349-115">Lokalizacja urządzenia</span><span class="sxs-lookup"><span data-stu-id="a8349-115">Location of the device</span></span>

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

### <span data-ttu-id="a8349-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8349-116">-Name</span></span>
<span data-ttu-id="a8349-117">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="a8349-117">Resource Name</span></span>

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

### <span data-ttu-id="a8349-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8349-118">-ResourceGroupName</span></span>
<span data-ttu-id="a8349-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a8349-119">Resource Group Name</span></span>

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

### <span data-ttu-id="a8349-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="a8349-120">-Sku</span></span>
<span data-ttu-id="a8349-121">Dostępne jednostki SKU to Edge, Brama</span><span class="sxs-lookup"><span data-stu-id="a8349-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="a8349-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8349-122">-Confirm</span></span>
<span data-ttu-id="a8349-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8349-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8349-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8349-124">-WhatIf</span></span>
<span data-ttu-id="a8349-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8349-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8349-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8349-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8349-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8349-127">CommonParameters</span></span>
<span data-ttu-id="a8349-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8349-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8349-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8349-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8349-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8349-130">INPUTS</span></span>

### <span data-ttu-id="a8349-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a8349-131">None</span></span>

## <span data-ttu-id="a8349-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8349-132">OUTPUTS</span></span>

### <span data-ttu-id="a8349-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a8349-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="a8349-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8349-134">NOTES</span></span>

## <span data-ttu-id="a8349-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8349-135">RELATED LINKS</span></span>
