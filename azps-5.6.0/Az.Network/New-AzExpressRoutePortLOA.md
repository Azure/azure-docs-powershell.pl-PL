---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: fc3780ea0e6cfff80117779786f1c9d9354ecf8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976698"
---
# <span data-ttu-id="f64d2-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="f64d2-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="f64d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f64d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f64d2-103">Pobierz dokument autoryzacji dla portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="f64d2-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="f64d2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f64d2-104">SYNTAX</span></span>

### <span data-ttu-id="f64d2-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f64d2-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f64d2-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f64d2-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f64d2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f64d2-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f64d2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f64d2-108">DESCRIPTION</span></span>
<span data-ttu-id="f64d2-109">New-AzExpressRoutePortLOA cmdlet pobiera dokument autoryzacji w formacie PDF dla portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="f64d2-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="f64d2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f64d2-110">EXAMPLES</span></span>

### <span data-ttu-id="f64d2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f64d2-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="f64d2-112">Pobierz dokument autoryzacji dla portu trasy ekspresowej "myPort" i przechowaj go w pliku "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="f64d2-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="f64d2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f64d2-113">PARAMETERS</span></span>

### <span data-ttu-id="f64d2-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f64d2-114">-AsJob</span></span>
<span data-ttu-id="f64d2-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f64d2-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f64d2-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="f64d2-116">-CustomerName</span></span>
<span data-ttu-id="f64d2-117">Nazwa klienta, do którego jest przypisany ten port trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="f64d2-117">The customer name to whom this Express Route Port is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64d2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f64d2-118">-DefaultProfile</span></span>
<span data-ttu-id="f64d2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f64d2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f64d2-120">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="f64d2-120">-Destination</span></span>
<span data-ttu-id="f64d2-121">Wyjściowa ścieżka pliku do przechowywania upoważnienia.</span><span class="sxs-lookup"><span data-stu-id="f64d2-121">The output filepath to store the Letter of Authorization to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64d2-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="f64d2-122">-ExpressRoutePort</span></span>
<span data-ttu-id="f64d2-123">Zasób portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="f64d2-123">The express route port resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64d2-124">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="f64d2-124">-Id</span></span>
<span data-ttu-id="f64d2-125">ResourceId portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="f64d2-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f64d2-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f64d2-126">-PassThru</span></span>
<span data-ttu-id="f64d2-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="f64d2-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f64d2-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="f64d2-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f64d2-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="f64d2-129">-PortName</span></span>
<span data-ttu-id="f64d2-130">Nazwa portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="f64d2-130">The express route port name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64d2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f64d2-131">-ResourceGroupName</span></span>
<span data-ttu-id="f64d2-132">Nazwa grupy zasobów dla portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="f64d2-132">The resource group name of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f64d2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f64d2-133">CommonParameters</span></span>
<span data-ttu-id="f64d2-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f64d2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f64d2-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f64d2-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f64d2-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f64d2-136">INPUTS</span></span>

### <span data-ttu-id="f64d2-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f64d2-137">System.String</span></span>

## <span data-ttu-id="f64d2-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f64d2-138">OUTPUTS</span></span>

### <span data-ttu-id="f64d2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f64d2-139">System.Boolean</span></span>

## <span data-ttu-id="f64d2-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f64d2-140">NOTES</span></span>

## <span data-ttu-id="f64d2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f64d2-141">RELATED LINKS</span></span>
