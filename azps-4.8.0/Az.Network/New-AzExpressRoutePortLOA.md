---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteportloa
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePortLOA.md
ms.openlocfilehash: 22f5023aa294dde734157439d8b355916adfb03f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223826"
---
# <span data-ttu-id="9b686-101">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="9b686-101">New-AzExpressRoutePortLOA</span></span>

## <span data-ttu-id="9b686-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b686-102">SYNOPSIS</span></span>
<span data-ttu-id="9b686-103">Pobieranie dokumentu autoryzacji dla portu usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="9b686-103">Download letter of authorization document for an express route port.</span></span>

## <span data-ttu-id="9b686-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b686-104">SYNTAX</span></span>

### <span data-ttu-id="9b686-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9b686-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePortLOA -PortName <String> -ResourceGroupName <String> -CustomerName <String>
 [-Destination <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b686-106">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b686-106">ResourceObjectParameterSet</span></span>
```
New-AzExpressRoutePortLOA -ExpressRoutePort <PSExpressRoutePort> -CustomerName <String> [-Destination <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b686-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b686-107">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePortLOA -Id <String> -CustomerName <String> [-Destination <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b686-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9b686-108">DESCRIPTION</span></span>
<span data-ttu-id="9b686-109">New-AzExpressRoutePortLOA polecenia cmdlet pobiera dokument autoryzacji listu w formacie PDF dla portu Express Route.</span><span class="sxs-lookup"><span data-stu-id="9b686-109">New-AzExpressRoutePortLOA cmdlet downloads a letter of authorization document in PDF format for an express route port.</span></span>


## <span data-ttu-id="9b686-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b686-110">EXAMPLES</span></span>

### <span data-ttu-id="9b686-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9b686-111">Example 1</span></span>
```powershell
PS C:\> New-AzExpressRoutePortLOA -ResourceGroupName myRg -PortName myPort -CustomerName Contoso -Destination loa.pdf
```

<span data-ttu-id="9b686-112">Pobierz dokument autoryzacji listu "Moja port" obiektu "mójMagazyn" i Zapisz go w pliku "loa.pdf".</span><span class="sxs-lookup"><span data-stu-id="9b686-112">Download the letter of authorization document for express route port 'myPort' and store it in file 'loa.pdf'.</span></span>

## <span data-ttu-id="9b686-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b686-113">PARAMETERS</span></span>

### <span data-ttu-id="9b686-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b686-114">-AsJob</span></span>
<span data-ttu-id="9b686-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="9b686-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b686-116">-CustomerName</span><span class="sxs-lookup"><span data-stu-id="9b686-116">-CustomerName</span></span>
<span data-ttu-id="9b686-117">Nazwa klienta, do którego jest przypisany dany port Express Route.</span><span class="sxs-lookup"><span data-stu-id="9b686-117">The customer name to whom this Express Route Port is assigned to.</span></span>

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

### <span data-ttu-id="9b686-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b686-118">-DefaultProfile</span></span>
<span data-ttu-id="9b686-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b686-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b686-120">-Miejsce docelowe</span><span class="sxs-lookup"><span data-stu-id="9b686-120">-Destination</span></span>
<span data-ttu-id="9b686-121">Ścieżka wyjściowa w celu zapisania listy autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="9b686-121">The output filepath to store the Letter of Authorization to.</span></span>

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

### <span data-ttu-id="9b686-122">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="9b686-122">-ExpressRoutePort</span></span>
<span data-ttu-id="9b686-123">Zasób portów usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="9b686-123">The express route port resource.</span></span>

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

### <span data-ttu-id="9b686-124">-ID</span><span class="sxs-lookup"><span data-stu-id="9b686-124">-Id</span></span>
<span data-ttu-id="9b686-125">Identyfikator zasobu Express Route port.</span><span class="sxs-lookup"><span data-stu-id="9b686-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="9b686-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b686-126">-PassThru</span></span>
<span data-ttu-id="9b686-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="9b686-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="9b686-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="9b686-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9b686-129">-Portname</span><span class="sxs-lookup"><span data-stu-id="9b686-129">-PortName</span></span>
<span data-ttu-id="9b686-130">Nazwa portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="9b686-130">The express route port name.</span></span>

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

### <span data-ttu-id="9b686-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b686-131">-ResourceGroupName</span></span>
<span data-ttu-id="9b686-132">Nazwa grupy zasobów portu usługi Express Route.</span><span class="sxs-lookup"><span data-stu-id="9b686-132">The resource group name of the express route port.</span></span>

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

### <span data-ttu-id="9b686-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b686-133">CommonParameters</span></span>
<span data-ttu-id="9b686-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b686-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b686-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b686-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b686-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b686-136">INPUTS</span></span>

### <span data-ttu-id="9b686-137">System. String</span><span class="sxs-lookup"><span data-stu-id="9b686-137">System.String</span></span>

## <span data-ttu-id="9b686-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b686-138">OUTPUTS</span></span>

### <span data-ttu-id="9b686-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b686-139">System.Boolean</span></span>

## <span data-ttu-id="9b686-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b686-140">NOTES</span></span>

## <span data-ttu-id="9b686-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b686-141">RELATED LINKS</span></span>
