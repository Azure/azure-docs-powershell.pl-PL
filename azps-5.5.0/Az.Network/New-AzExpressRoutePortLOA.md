---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187075"
---
# <span data-ttu-id="288ed-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="288ed-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="288ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="288ed-102">SYNOPSIS</span></span>
<span data-ttu-id="288ed-103">Pobierz dokument autoryzacji dla portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="288ed-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="288ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="288ed-104">SYNTAX</span></span>

### <span data-ttu-id="288ed-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="288ed-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="288ed-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="288ed-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="288ed-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="288ed-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="288ed-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="288ed-108">DESCRIPTION</span></span>
<span data-ttu-id="288ed-109">New-AzExpressRoutePortLOA cmdlet pobiera dokument autoryzacji w formacie PDF dla portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="288ed-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="288ed-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="288ed-110">EXAMPLES</span></span>

### <span data-ttu-id="288ed-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="288ed-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="288ed-112">Pobierz dokument autoryzacji dla portu trasy ekspresowej "myPort" i przechowaj go w pliku "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="288ed-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="288ed-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="288ed-113">PARAMETERS</span></span>

### <span data-ttu-id="288ed-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="288ed-114">-AsJob</span></span>
<span data-ttu-id="288ed-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="288ed-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="288ed-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="288ed-116">-CustomerName</span></span>
<span data-ttu-id="288ed-117">Nazwa klienta, do którego jest przypisany ten port trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="288ed-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="288ed-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="288ed-118">-DefaultProfile</span></span>
<span data-ttu-id="288ed-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="288ed-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="288ed-120">— miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="288ed-120">-Destination</span></span>
<span data-ttu-id="288ed-121">Wyjściowa ścieżka pliku do przechowywania upoważnienia.</span><span class="sxs-lookup"><span data-stu-id="288ed-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="288ed-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="288ed-122">-ExpressRoutePort</span></span>
<span data-ttu-id="288ed-123">Zasób portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="288ed-123">The express route port resource.</span></span>

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

### <span data-ttu-id="288ed-124">— Id</span><span class="sxs-lookup"><span data-stu-id="288ed-124">-Id</span></span>
<span data-ttu-id="288ed-125">ResourceId portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="288ed-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="288ed-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="288ed-126">-PassThru</span></span>
<span data-ttu-id="288ed-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="288ed-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="288ed-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="288ed-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="288ed-129">-PortName</span><span class="sxs-lookup"><span data-stu-id="288ed-129">-PortName</span></span>
<span data-ttu-id="288ed-130">Nazwa portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="288ed-130">The express route port name.</span></span>

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

### <span data-ttu-id="288ed-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="288ed-131">-ResourceGroupName</span></span>
<span data-ttu-id="288ed-132">Nazwa grupy zasobów dla portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="288ed-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="288ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="288ed-133">CommonParameters</span></span>
<span data-ttu-id="288ed-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="288ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="288ed-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="288ed-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="288ed-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="288ed-136">INPUTS</span></span>

### <span data-ttu-id="288ed-137">System.String</span><span class="sxs-lookup"><span data-stu-id="288ed-137">System.String</span></span>

## <span data-ttu-id="288ed-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="288ed-138">OUTPUTS</span></span>

### <span data-ttu-id="288ed-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="288ed-139">System.Boolean</span></span>

## <span data-ttu-id="288ed-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="288ed-140">NOTES</span></span>

## <span data-ttu-id="288ed-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="288ed-141">RELATED LINKS</span></span>
