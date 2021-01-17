---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeDevice.md
ms.openlocfilehash: d26482607dafb10de5b9990b003493ca81fc9ccf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335410"
---
# <span data-ttu-id="811e9-101">New-AzStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="811e9-101">New-AzStackEdgeDevice</span></span>

## <span data-ttu-id="811e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="811e9-102">SYNOPSIS</span></span>
<span data-ttu-id="811e9-103">Konfiguruje nowe urządzenie brzegowe stosu</span><span class="sxs-lookup"><span data-stu-id="811e9-103">Configures a new Stack Edge device</span></span>

## <span data-ttu-id="811e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="811e9-104">SYNTAX</span></span>

```
New-AzStackEdgeDevice [-ResourceGroupName] <String> [-Name] <String> -Location <String> -Sku <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="811e9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="811e9-105">DESCRIPTION</span></span>
<span data-ttu-id="811e9-106">Polecenie cmdlet **New-AzStackEdgeDevice** konfiguruje nowe urządzenie brzegowe stosujące</span><span class="sxs-lookup"><span data-stu-id="811e9-106">The **New-AzStackEdgeDevice** cmdlet configures a new Stack Edge device</span></span>

## <span data-ttu-id="811e9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="811e9-107">EXAMPLES</span></span>

### <span data-ttu-id="811e9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="811e9-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeDevice -ResourceGroupName resourceGroupName -Name deviceName -Location eastus -Sku Edge
Name            ResourceGroupName    Model   Location
----            -----------------    -----   --------
deviceName      resourceGroupName    Edge    eastus
```

## <span data-ttu-id="811e9-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="811e9-109">PARAMETERS</span></span>

### <span data-ttu-id="811e9-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="811e9-110">-AsJob</span></span>
<span data-ttu-id="811e9-111">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="811e9-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="811e9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="811e9-112">-DefaultProfile</span></span>
<span data-ttu-id="811e9-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="811e9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="811e9-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="811e9-114">-Location</span></span>
<span data-ttu-id="811e9-115">Lokalizacja urządzenia</span><span class="sxs-lookup"><span data-stu-id="811e9-115">Location of the device</span></span>

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

### <span data-ttu-id="811e9-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="811e9-116">-Name</span></span>
<span data-ttu-id="811e9-117">Nazwa zasobu</span><span class="sxs-lookup"><span data-stu-id="811e9-117">Resource Name</span></span>

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

### <span data-ttu-id="811e9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="811e9-118">-ResourceGroupName</span></span>
<span data-ttu-id="811e9-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="811e9-119">Resource Group Name</span></span>

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

### <span data-ttu-id="811e9-120">-SKU</span><span class="sxs-lookup"><span data-stu-id="811e9-120">-Sku</span></span>
<span data-ttu-id="811e9-121">Dostępne jednostki SKU to Edge, Brama</span><span class="sxs-lookup"><span data-stu-id="811e9-121">Available Skus are Edge, Gateway</span></span>

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

### <span data-ttu-id="811e9-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="811e9-122">-Confirm</span></span>
<span data-ttu-id="811e9-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="811e9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="811e9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="811e9-124">-WhatIf</span></span>
<span data-ttu-id="811e9-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="811e9-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="811e9-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="811e9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="811e9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="811e9-127">CommonParameters</span></span>
<span data-ttu-id="811e9-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="811e9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="811e9-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="811e9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="811e9-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="811e9-130">INPUTS</span></span>

### <span data-ttu-id="811e9-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="811e9-131">None</span></span>

## <span data-ttu-id="811e9-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="811e9-132">OUTPUTS</span></span>

### <span data-ttu-id="811e9-133">Microsoft. Azure. PowerShell. polecenia. StackEdge. models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="811e9-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="811e9-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="811e9-134">NOTES</span></span>

## <span data-ttu-id="811e9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="811e9-135">RELATED LINKS</span></span>
